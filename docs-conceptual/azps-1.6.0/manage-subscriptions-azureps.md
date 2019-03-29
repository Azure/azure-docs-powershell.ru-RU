---
title: Управление подписками Azure с помощью Azure PowerShell
description: Управление подписками Azure с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475424"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="e0fe2-103">Использование нескольких подписок Azure</span><span class="sxs-lookup"><span data-stu-id="e0fe2-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="e0fe2-104">Большинство пользователей Azure обычно используют только одну подписку.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="e0fe2-105">Но если вы работаете в нескольких организациях или если доступ к определенным ресурсам в вашей организации разделен по группам, у вас может быть несколько подписок Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="e0fe2-106">CLI поддерживает выбор подписки как глобально, так и для отдельных команд.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-106">The CLI supports selecting a subscription both globally and per command.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="e0fe2-107">Клиенты, пользователи и подписки</span><span class="sxs-lookup"><span data-stu-id="e0fe2-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="e0fe2-108">При определении различий между клиентами, пользователями и подписками в Azure может возникнуть путаница.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="e0fe2-109">_Клиент_ — это сущность Azure Active Directory, которая условно представляет всю организацию.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-109">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="e0fe2-110">Клиент предполагает наличие минимум одной _подписки_ и одного _пользователя_.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="e0fe2-111">Пользователь — это человек, который связан только с одним клиентом — организацией, в которой он работает.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="e0fe2-112">Пользователи — это учетные записи для входа в Azure, которые используются, чтобы создавать, использовать и администрировать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-112">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="e0fe2-113">Пользователь может иметь доступ к нескольким _подпискам_. Подписки — это соглашения с корпорацией Майкрософт на использование облачных служб, в том числе Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="e0fe2-114">Каждый ресурс связан с подпиской.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="e0fe2-115">Дополнительные сведения о различиях между клиентами, пользователями и подписками см. в [словаре терминов, связанных с облачной платформой Azure](/azure/azure-glossary-cloud-terminology).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="e0fe2-116">Чтобы узнать, как добавить новую подписку в клиент Azure Active Directory, см. статью [Как добавить подписку Azure в Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="e0fe2-117">Сведения о том, как выполнить вход от имени определенного клиента см. в статье [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps) (Вход с помощью Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-117">To learn how to sign in to a specific tenant, see [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="e0fe2-118">Изменение активной подписки</span><span class="sxs-lookup"><span data-stu-id="e0fe2-118">Change the active subscription</span></span>

<span data-ttu-id="e0fe2-119">Доступ к ресурсам для подписки в Azure PowerShell требует изменения подписки, связанной с вашим текущим сеансом Azure.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-119">In Azure PowerShell, accessing the resources for a subscription requires changing the subscription associated with your current Azure session.</span></span>
<span data-ttu-id="e0fe2-120">Чтобы сделать это, измените активный контекст сеанса (данные о том, для каких клиента, подписки и пользователя необходимо выполнить командлеты).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-120">This is done by modifying the active session context, the information about which tenant, subscription, and user cmdlets should be run against.</span></span>
<span data-ttu-id="e0fe2-121">Чтобы изменить подписки, сначала нужно извлечь объект контекста Azure PowerShell с помощью командлета [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), а затем изменить текущий контекст с помощью командлета [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-121">In order to change subscriptions, an Azure PowerShell Context object first needs to be retrieved with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and then the current context changed with [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span></span>

<span data-ttu-id="e0fe2-122">В следующем примере показано, как получить подписку активного клиента и установить ее в качестве активного сеанса.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-122">The next example shows how to get a subscription in the currently active tenant, and set it as the active session:</span></span>

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

<span data-ttu-id="e0fe2-123">Дополнительные сведения о контекстах Azure PowerShell, в том числе о том, как сохранять их и быстро переключаться между ними для удобной работы с несколькими подписками, см. в статье [Persist credentials with Azure PowerShell contexts](context-persistence.md) (Сохранение учетных данных с контекстами Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-123">To learn more about Azure PowerShell contexts, including how to save them and quickly switch between them for working with multiple subscriptions easily, see [Persist credentials with Azure PowerShell contexts](context-persistence.md).</span></span>