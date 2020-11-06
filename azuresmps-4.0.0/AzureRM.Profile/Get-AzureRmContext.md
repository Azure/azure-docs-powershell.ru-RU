---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555635"
---
# <span data-ttu-id="f172a-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="f172a-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="f172a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f172a-102">SYNOPSIS</span></span>
<span data-ttu-id="f172a-103">Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f172a-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="f172a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f172a-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="f172a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f172a-105">DESCRIPTION</span></span>
<span data-ttu-id="f172a-106">Командлет Get-AzureRmContext получает текущие метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f172a-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="f172a-107">Этот командлет получает учетную запись Active Directory, клиента Active Directory, подписку на Azure и целевую среду Azure.</span><span class="sxs-lookup"><span data-stu-id="f172a-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="f172a-108">Командлеты диспетчера ресурсов Azure по умолчанию используют эти параметры при выполнении запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f172a-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="f172a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f172a-109">EXAMPLES</span></span>

### <span data-ttu-id="f172a-110">Пример 1: Загрузка текущего контекста</span><span class="sxs-lookup"><span data-stu-id="f172a-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="f172a-111">В этом примере мы используем подписку на Azure для входа в нашу учетную запись с помощью Add-AzureRmAccount, а затем получили контекст текущего сеанса, вызвав Get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="f172a-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="f172a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f172a-112">PARAMETERS</span></span>

### <span data-ttu-id="f172a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f172a-113">CommonParameters</span></span>
<span data-ttu-id="f172a-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f172a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f172a-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f172a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f172a-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f172a-116">INPUTS</span></span>

## <span data-ttu-id="f172a-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f172a-117">OUTPUTS</span></span>

### <span data-ttu-id="f172a-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f172a-118">PSAzureContext</span></span>
<span data-ttu-id="f172a-119">Этот командлет возвращает учетную запись, клиента и подписку, используемые командлетами диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f172a-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="f172a-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="f172a-120">NOTES</span></span>

## <span data-ttu-id="f172a-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f172a-121">RELATED LINKS</span></span>

[<span data-ttu-id="f172a-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="f172a-122">Set-AzureRMContext</span></span>]()

