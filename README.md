import React, { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function HomePage() {
  const [language, setLanguage] = useState("ca");

  const texts = {
    ca: {
      title: "evolveX AI automation",
      subtitle: "Escala la teva empresa amb automatització intel·ligent",
      slogan: "El futur de l'hostaleria comença amb l'automatització",
      who: "Qui som",
      team: "El nostre equip",
      teamText: "Som tres estudiants emprenedors apassionats per la tecnologia i la innovació aplicades al sector de l’hostaleria.",
      mission: "La nostra missió",
      missionText: "Volem millorar l’eficiència dels negocis d’hostaleria mitjançant l’automatització intel·ligent.",
      why: "Per què evolveX AI?",
      whyText: "Ens diferenciem per oferir un sistema intel·ligent que automatitza trucades reals, estalviant temps i diners als negocis.",
      services: "Serveis",
      booking: "Automatització de reserves",
      bookingText: "Gestió automàtica de reserves per telèfon sense necessitat d’intervenció humana.",
      support: "Atenció al client 24/7",
      supportText: "Resposta automàtica a preguntes freqüents i assistència telefònica les 24 hores del dia.",
      contact: "Contacte",
      contactText: "Per a col·laboracions o més informació, contacta amb nosaltres:",
      email: "Email",
      phone: "Telèfon",
      message: "Enviar un missatge"
    },
    en: {
      title: "evolveX AI automation",
      subtitle: "Scale your business with intelligent automation",
      slogan: "The future of hospitality starts with automation",
      who: "About us",
      team: "Our team",
      teamText: "We are three student entrepreneurs passionate about technology and innovation applied to the hospitality sector.",
      mission: "Our mission",
      missionText: "We aim to improve business efficiency in hospitality through smart automation.",
      why: "Why evolveX AI?",
      whyText: "We stand out by offering an intelligent system that automates real calls, saving businesses time and money.",
      services: "Services",
      booking: "Reservation automation",
      bookingText: "Automatic phone reservation management with no human intervention needed.",
      support: "24/7 Customer Support",
      supportText: "Automatic response to FAQs and phone support 24/7.",
      contact: "Contact",
      contactText: "For collaborations or more information, contact us:",
      email: "Email",
      phone: "Phone",
      message: "Send a message"
    }
  };

  const t = texts[language];

  return (
    <div className="min-h-screen bg-white text-gray-900">
      {/* Canvi d'idioma */}
      <div className="absolute top-4 right-4 space-x-2">
        <Button variant="outline" onClick={() => setLanguage("ca")}>Català</Button>
        <Button variant="outline" onClick={() => setLanguage("en")}>English</Button>
      </div>

      {/* Pàgina principal */}
      <section className="flex flex-col items-center justify-center h-screen bg-gray-100 text-center px-4">
        <h1 className="text-5xl font-bold mb-4">{t.title}</h1>
        <p className="text-xl mb-2">{t.subtitle}</p>
        <p className="text-lg italic text-gray-600">{t.slogan}</p>
      </section>

      {/* Qui som */}
      <section className="py-20 px-6 bg-white" id="qui-som">
        <h2 className="text-4xl font-bold mb-8 text-center">{t.who}</h2>
        <div className="max-w-4xl mx-auto space-y-6">
          <Card>
            <CardContent className="p-6">
              <h3 className="text-2xl font-semibold mb-2">{t.team}</h3>
              <p>{t.teamText}</p>
            </CardContent>
          </Card>
          <Card>
            <CardContent className="p-6">
              <h3 className="text-2xl font-semibold mb-2">{t.mission}</h3>
              <p>{t.missionText}</p>
            </CardContent>
          </Card>
          <Card>
            <CardContent className="p-6">
              <h3 className="text-2xl font-semibold mb-2">{t.why}</h3>
              <p>{t.whyText}</p>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Serveis */}
      <section className="py-20 px-6 bg-gray-50" id="serveis">
        <h2 className="text-4xl font-bold mb-8 text-center">{t.services}</h2>
        <div className="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-6">
          <Card>
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">{t.booking}</h3>
              <p>{t.bookingText}</p>
            </CardContent>
          </Card>
          <Card>
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">{t.support}</h3>
              <p>{t.supportText}</p>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Contacte */}
      <section className="py-20 px-6 bg-white" id="contacte">
        <h2 className="text-4xl font-bold mb-8 text-center">{t.contact}</h2>
        <div className="max-w-xl mx-auto space-y-4">
          <p className="text-center">{t.contactText}</p>
          <div className="text-center">
            <p>{t.email}: <a href="mailto:contacte@evolvex.ai" className="text-blue-600">contacte@evolvex.ai</a></p>
            <p>{t.phone}: <a href="tel:+34930000000" className="text-blue-600">+34 930 00 00 00</a></p>
          </div>
          <div className="text-center mt-4">
            <Button>{t.message}</Button>
          </div>
        </div>
      </section>
    </div>
  );
}
