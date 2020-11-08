---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075216"
---
# <span data-ttu-id="69923-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="69923-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="69923-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69923-102">SYNOPSIS</span></span>
<span data-ttu-id="69923-103">Получение списка всех объектов квот для KeyVault в местоположении.</span><span class="sxs-lookup"><span data-stu-id="69923-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="69923-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69923-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="69923-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69923-105">DESCRIPTION</span></span>
<span data-ttu-id="69923-106">Получение списка всех объектов квот для KeyVault в местоположении.</span><span class="sxs-lookup"><span data-stu-id="69923-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="69923-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69923-107">EXAMPLES</span></span>

### <span data-ttu-id="69923-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="69923-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="69923-109">Получение списка всех объектов квот для KeyVault в местоположении.</span><span class="sxs-lookup"><span data-stu-id="69923-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="69923-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69923-110">PARAMETERS</span></span>

### <span data-ttu-id="69923-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69923-111">-DefaultProfile</span></span>
<span data-ttu-id="69923-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69923-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69923-113">-Location</span><span class="sxs-lookup"><span data-stu-id="69923-113">-Location</span></span>
<span data-ttu-id="69923-114">Расположение квоты.</span><span class="sxs-lookup"><span data-stu-id="69923-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69923-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69923-115">-SubscriptionId</span></span>
<span data-ttu-id="69923-116">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="69923-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="69923-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69923-117">CommonParameters</span></span>
<span data-ttu-id="69923-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69923-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69923-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69923-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69923-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69923-120">INPUTS</span></span>

## <span data-ttu-id="69923-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69923-121">OUTPUTS</span></span>

### <span data-ttu-id="69923-122">Microsoft. Azure. PowerShell. командлеты. KeyVaultAdmin. Models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="69923-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="69923-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="69923-123">NOTES</span></span>

## <span data-ttu-id="69923-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69923-124">RELATED LINKS</span></span>

