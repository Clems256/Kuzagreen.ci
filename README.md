import React, { useState } from 'react';
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Leaf, Recycle, Droplets, Sun, Users, ArrowRight } from 'lucide-react';

const KuzaGreenWebsite = () => {
  const [activeTab, setActiveTab] = useState('home');

  const initiatives = [
    {
      title: "Gestion des Déchets",
      icon: <Recycle className="w-8 h-8 text-green-600" />,
      description: "Apprenez les meilleures pratiques de tri et recyclage des déchets"
    },
    {
      title: "Conservation de l'Eau",
      icon: <Droplets className="w-8 h-8 text-blue-600" />,
      description: "Techniques pour préserver nos ressources en eau"
    },
    {
      title: "Énergie Renouvelable",
      icon: <Sun className="w-8 h-8 text-yellow-600" />,
      description: "Solutions d'énergie propre pour nos communautés"
    },
    {
      title: "Agriculture Durable",
      icon: <Leaf className="w-8 h-8 text-green-700" />,
      description: "Méthodes traditionnelles et modernes pour une agriculture responsable"
    }
  ];

  return (
    <div className="min-h-screen bg-gray-50">
      {/* Hero Section */}
      <header className="bg-green-700 text-white py-12">
        <div className="container mx-auto px-4">
          <h1 className="text-4xl font-bold mb-4">KuzaGreen Côte d'Ivoire</h1>
          <p className="text-xl mb-8">Ensemble pour un environnement durable</p>
          <button className="bg-white text-green-700 px-6 py-2 rounded-full font-semibold hover:bg-green-100 flex items-center gap-2">
            Rejoignez le mouvement
            <ArrowRight className="w-4 h-4" />
          </button>
        </div>
      </header>

      {/* Main Content */}
      <main className="container mx-auto px-4 py-12">
        {/* Initiatives Section */}
        <section className="mb-16">
          <h2 className="text-3xl font-bold mb-8 text-center">Nos Initiatives</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            {initiatives.map((initiative, index) => (
              <Card key={index} className="hover:shadow-lg transition-shadow">
                <CardHeader className="text-center">
                  <div className="mx-auto mb-4">{initiative.icon}</div>
                  <CardTitle className="text-xl font-bold">{initiative.title}</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-gray-600 text-center">{initiative.description}</p>
                </CardContent>
              </Card>
            ))}
          </div>
        </section>

        {/* Community Impact Section */}
        <section className="mb-16">
          <Card className="bg-green-50">
            <CardContent className="p-8">
              <div className="flex items-center justify-between flex-wrap gap-8">
                <div className="text-center flex-1">
                  <h3 className="text-4xl font-bold text-green-700 mb-2">1000+</h3>
                  <p className="text-gray-600">Arbres Plantés</p>
                </div>
                <div className="text-center flex-1">
                  <h3 className="text-4xl font-bold text-green-700 mb-2">500+</h3>
                  <p className="text-gray-600">Participants</p>
                </div>
                <div className="text-center flex-1">
                  <h3 className="text-4xl font-bold text-green-700 mb-2">10</h3>
                  <p className="text-gray-600">Communautés</p>
                </div>
                <div className="text-center flex-1">
                  <h3 className="text-4xl font-bold text-green-700 mb-2">5+</h3>
                  <p className="text-gray-600">Programmes Actifs</p>
                </div>
              </div>
            </CardContent>
          </Card>
        </section>

        {/* Get Involved Section */}
        <section>
          <h2 className="text-3xl font-bold mb-8 text-center">Comment Participer</h2>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Users className="w-6 h-6 text-green-600" />
                  Rejoignez une Communauté
                </CardTitle>
              </CardHeader>
              <CardContent>
                <p className="text-gray-600">Connectez-vous avec d'autres passionnés de l'environnement dans votre région</p>
              </CardContent>
            </Card>
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Leaf className="w-6 h-6 text-green-600" />
                  Participez aux Projets
                </CardTitle>
              </CardHeader>
              <CardContent>
                <p className="text-gray-600">Engagez-vous dans nos initiatives de plantation et de sensibilisation</p>
              </CardContent>
            </Card>
            <Card>
              <CardHeader>
                <CardTitle className="flex items-center gap-2">
                  <Sun className="w-6 h-6 text-green-600" />
                  Partagez vos Connaissances
                </CardTitle>
              </CardHeader>
              <CardContent>
                <p className="text-gray-600">Transmettez votre expertise et vos expériences à la communauté</p>
              </CardContent>
            </Card>
          </div>
        </section>
      </main>

      {/* Footer */}
      <footer className="bg-green-800 text-white py-8">
        <div className="container mx-auto px-4">
          <div className="text-center">
            <h3 className="text-2xl font-bold mb-4">KuzaGreen</h3>
            <p className="mb-4">Ensemble pour un avenir plus vert en Côte d'Ivoire</p>
            <div className="flex justify-center gap-4">
              <button className="hover:text-green-300">Contact</button>
              <button className="hover:text-green-300">À Propos</button>
              <button className="hover:text-green-300">Mentions Légales</button>
            </div>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default KuzaGreenWebsite;
