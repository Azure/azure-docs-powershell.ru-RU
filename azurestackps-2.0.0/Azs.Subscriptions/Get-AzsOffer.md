---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911606"
---
# <span data-ttu-id="df12d-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="df12d-101">Get-AzsOffer</span></span>

## <span data-ttu-id="df12d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df12d-102">SYNOPSIS</span></span>
<span data-ttu-id="df12d-103">Получение списка открытых предложений для корневого поставщика.</span><span class="sxs-lookup"><span data-stu-id="df12d-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="df12d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df12d-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="df12d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df12d-105">DESCRIPTION</span></span>
<span data-ttu-id="df12d-106">Получение списка открытых предложений для корневого поставщика.</span><span class="sxs-lookup"><span data-stu-id="df12d-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="df12d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df12d-107">EXAMPLES</span></span>

### <span data-ttu-id="df12d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df12d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="df12d-109">Получение списка открытых предложений</span><span class="sxs-lookup"><span data-stu-id="df12d-109">Get the list of public offers</span></span>

## <span data-ttu-id="df12d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df12d-110">PARAMETERS</span></span>

### <span data-ttu-id="df12d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df12d-111">-DefaultProfile</span></span>
<span data-ttu-id="df12d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df12d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="df12d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df12d-113">CommonParameters</span></span>
<span data-ttu-id="df12d-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df12d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df12d-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df12d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df12d-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df12d-116">INPUTS</span></span>

## <span data-ttu-id="df12d-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df12d-117">OUTPUTS</span></span>

### <span data-ttu-id="df12d-118">Microsoft. Azure. PowerShell. командлеты. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="df12d-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="df12d-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="df12d-119">NOTES</span></span>

## <span data-ttu-id="df12d-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df12d-120">RELATED LINKS</span></span>

