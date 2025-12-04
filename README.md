import React from 'react';
import Header from './components/Header';
import Footer from './components/Footer';
import AppCard from './components/AppCard';
import { APPS } from './constants';

const App: React.FC = () => {
  return (
    <div className="min-h-screen flex flex-col">
      <Header />

      <main className="flex-grow w-full max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
        
        {/* Intro Section */}
        <div className="text-center max-w-2xl mx-auto mb-12">
          <div className="bg-blue-50 text-blue-800 text-sm font-semibold py-1 px-4 rounded-full inline-block mb-4 shadow-sm border border-blue-100">
            Status: Online & Working
          </div>
          <h2 className="text-2xl sm:text-3xl font-bold text-gray-800 mb-4">
            Select Your Application
          </h2>
          <p className="text-gray-600 text-lg">
            Choose an app below to start downloading. Verification is required to unlock access to these premium features.
          </p>
        </div>

        {/* App Grid */}
        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 sm:gap-8">
          {APPS.map((app) => (
            <AppCard key={app.id} app={app} />
          ))}
        </div>

        {/* Trust Indicators */}
        <div className="mt-16 grid grid-cols-2 md:grid-cols-4 gap-4 text-center">
             <div className="bg-white p-4 rounded-xl shadow-sm border border-gray-100">
                <div className="text-2xl mb-1">🔒</div>
                <div className="text-xs font-bold text-gray-700">SSL Secure</div>
             </div>
             <div className="bg-white p-4 rounded-xl shadow-sm border border-gray-100">
                <div className="text-2xl mb-1">⚡</div>
                <div className="text-xs font-bold text-gray-700">Fast Speed</div>
             </div>
             <div className="bg-white p-4 rounded-xl shadow-sm border border-gray-100">
                <div className="text-2xl mb-1">✅</div>
                <div className="text-xs font-bold text-gray-700">Verified</div>
             </div>
             <div className="bg-white p-4 rounded-xl shadow-sm border border-gray-100">
                <div className="text-2xl mb-1">📱</div>
                <div className="text-xs font-bold text-gray-700">Mobile Ready</div>
             </div>
        </div>
      </main>

      <Footer />
    </div>
  );
};

export default App;
