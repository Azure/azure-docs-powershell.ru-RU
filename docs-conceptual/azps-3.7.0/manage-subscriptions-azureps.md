---
title: Управление подписками Azure с помощью Azure PowerShell
description: Управление подписками Azure с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 778fdb463a42b609d3a94c910a2c0f9553ef4eb9
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440713"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="d4737-103">Использование нескольких подписок Azure</span><span class="sxs-lookup"><span data-stu-id="d4737-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="d4737-104">Большинство пользователей Azure обычно используют только одну подписку.</span><span class="sxs-lookup"><span data-stu-id="d4737-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="d4737-105">Но если вы работаете в нескольких организациях или если доступ к определенным ресурсам в вашей организации разделен по группам, у вас может быть несколько подписок Azure.</span><span class="sxs-lookup"><span data-stu-id="d4737-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="d4737-106">CLI поддерживает выбор подписки как глобально, так и для отдельных команд.</span><span class="sxs-lookup"><span data-stu-id="d4737-106">The CLI supports selecting a subscription both globally and per command.</span></span>

<span data-ttu-id="d4737-107">См. подробнее о [подписках, выставлении счетов и управлении затратами](/azure/billing/).</span><span class="sxs-lookup"><span data-stu-id="d4737-107">For detailed information on subscriptions, billing, and cost management, see the [billing and cost management documentation](/azure/billing/).</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="d4737-108">Клиенты, пользователи и подписки</span><span class="sxs-lookup"><span data-stu-id="d4737-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="d4737-109">При определении различий между клиентами, пользователями и подписками в Azure может возникнуть путаница.</span><span class="sxs-lookup"><span data-stu-id="d4737-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="d4737-110">_Клиент_ — это сущность Azure Active Directory, которая условно представляет всю организацию.</span><span class="sxs-lookup"><span data-stu-id="d4737-110">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="d4737-111">Клиент предполагает наличие минимум одной _подписки_ и одного _пользователя_.</span><span class="sxs-lookup"><span data-stu-id="d4737-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="d4737-112">Пользователь — это человек, который связан только с одним клиентом — организацией, в которой он работает.</span><span class="sxs-lookup"><span data-stu-id="d4737-112">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="d4737-113">Пользователи — это учетные записи для входа в Azure, которые используются, чтобы создавать, использовать и администрировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d4737-113">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="d4737-114">Пользователь может иметь доступ к нескольким _подпискам_. Подписки — это соглашения с корпорацией Майкрософт на использование облачных служб, в том числе Azure.</span><span class="sxs-lookup"><span data-stu-id="d4737-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="d4737-115">Каждый ресурс связан с подпиской.</span><span class="sxs-lookup"><span data-stu-id="d4737-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="d4737-116">Дополнительные сведения о различиях между клиентами, пользователями и подписками см. в [словаре терминов, связанных с облачной платформой Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="d4737-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="d4737-117">Чтобы узнать, как добавить новую подписку в клиент Azure Active Directory, см. статью [Как добавить подписку Azure в Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="d4737-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="d4737-118">Сведения о том, как выполнить вход от имени определенного клиента см. в статье [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps) (Вход с помощью Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="d4737-118">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="d4737-119">Изменение активной подписки</span><span class="sxs-lookup"><span data-stu-id="d4737-119">Change the active subscription</span></span>

<span data-ttu-id="d4737-120">Доступ к ресурсам для подписки в Azure PowerShell требует изменения подписки, связанной с вашим текущим сеансом Azure.</span><span class="sxs-lookup"><span data-stu-id="d4737-120">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="d4737-121">Чтобы сделать это, измените активный контекст сеанса (данные о том, для каких клиента, подписки и пользователя необходимо выполнить командлеты).</span><span class="sxs-lookup"><span data-stu-id="d4737-121">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="d4737-122">Чтобы изменить подписки, сначала нужно извлечь объект контекста Azure PowerShell с помощью командлета [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), а затем изменить текущий контекст с помощью командлета [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="d4737-122">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="d4737-123">В следующем примере показано, как получить подписку активного клиента и установить ее в качестве активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="d4737-123">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="d4737-124">Дополнительные сведения о контекстах Azure PowerShell, в том числе о том, как сохранять их и быстро переключаться между ними для удобной работы с несколькими подписками, см. в статье [Persist credentials with Azure PowerShell contexts](context-persistence.md) (Сохранение учетных данных с контекстами Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="d4737-124">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>
