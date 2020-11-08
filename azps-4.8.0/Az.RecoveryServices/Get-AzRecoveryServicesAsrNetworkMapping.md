---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235480"
---
# <span data-ttu-id="7e0d8-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e0d8-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="7e0d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0d8-103">Получение сведений о сопоставлениях сети восстановления сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="7e0d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e0d8-104">SYNTAX</span></span>

### <span data-ttu-id="7e0d8-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e0d8-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e0d8-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="7e0d8-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-107">DESCRIPTION</span></span>
<span data-ttu-id="7e0d8-108">Командлет **Get-AzRecoveryServicesAsrNetworkMapping** получает сведения о сопоставлениях сети восстановления сайта Azure для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="7e0d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0d8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e0d8-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="7e0d8-111">Возвращает все сопоставления сетей для переданной сети.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="7e0d8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7e0d8-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="7e0d8-113">Получает сопоставление сетей с предоставленным именем в указанной структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="7e0d8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-114">PARAMETERS</span></span>

### <span data-ttu-id="7e0d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0d8-115">-DefaultProfile</span></span>
<span data-ttu-id="7e0d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0d8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e0d8-117">-Name</span></span>
<span data-ttu-id="7e0d8-118">Имя получаемого объекта сетевого сопоставления ASR.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e0d8-119">-Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="7e0d8-119">-Network</span></span>
<span data-ttu-id="7e0d8-120">Получение сетевых сопоставлений ASR, соответствующих указанному объекту сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0d8-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7e0d8-121">-PrimaryFabric</span></span>
<span data-ttu-id="7e0d8-122">Получение сетевых сопоставлений ASR, соответствующих заданному основному объекту фабрики.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0d8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0d8-123">CommonParameters</span></span>
<span data-ttu-id="7e0d8-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0d8-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e0d8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0d8-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e0d8-126">INPUTS</span></span>

### <span data-ttu-id="7e0d8-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="7e0d8-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="7e0d8-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7e0d8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7e0d8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-129">OUTPUTS</span></span>

### <span data-ttu-id="7e0d8-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e0d8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="7e0d8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e0d8-131">NOTES</span></span>

## <span data-ttu-id="7e0d8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e0d8-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e0d8-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="7e0d8-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e0d8-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)