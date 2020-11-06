---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 442fd62393b33cc69e8f5a38f726bb8816c5bc64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561628"
---
# <span data-ttu-id="2efb7-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2efb7-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="2efb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2efb7-102">SYNOPSIS</span></span>
<span data-ttu-id="2efb7-103">Получение сведений о сопоставлениях сети восстановления сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2efb7-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2efb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2efb7-104">SYNTAX</span></span>

### <span data-ttu-id="2efb7-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2efb7-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2efb7-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="2efb7-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2efb7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2efb7-107">DESCRIPTION</span></span>
<span data-ttu-id="2efb7-108">Командлет **Get-AzureRmRecoveryServicesAsrNetworkMapping** получает сведения о сопоставлениях сети восстановления сайта Azure для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2efb7-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="2efb7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2efb7-109">EXAMPLES</span></span>

### <span data-ttu-id="2efb7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2efb7-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="2efb7-111">Возвращает все сопоставления сетей для переданной сети.</span><span class="sxs-lookup"><span data-stu-id="2efb7-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="2efb7-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2efb7-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="2efb7-113">Получает сопоставление сетей с предоставленным именем в указанной структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="2efb7-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="2efb7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2efb7-114">PARAMETERS</span></span>

### <span data-ttu-id="2efb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efb7-115">-DefaultProfile</span></span>
<span data-ttu-id="2efb7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2efb7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efb7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2efb7-117">-Name</span></span>
<span data-ttu-id="2efb7-118">Имя получаемого объекта сетевого сопоставления ASR.</span><span class="sxs-lookup"><span data-stu-id="2efb7-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efb7-119">-Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="2efb7-119">-Network</span></span>
<span data-ttu-id="2efb7-120">Получение сетевых сопоставлений ASR, соответствующих указанному объекту сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="2efb7-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb7-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="2efb7-121">-PrimaryFabric</span></span>
<span data-ttu-id="2efb7-122">Получение сетевых сопоставлений ASR, соответствующих заданному основному объекту фабрики.</span><span class="sxs-lookup"><span data-stu-id="2efb7-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efb7-123">CommonParameters</span></span>
<span data-ttu-id="2efb7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2efb7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efb7-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2efb7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efb7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2efb7-126">INPUTS</span></span>

### <span data-ttu-id="2efb7-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2efb7-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2efb7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2efb7-128">OUTPUTS</span></span>

### <span data-ttu-id="2efb7-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="2efb7-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2efb7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2efb7-130">NOTES</span></span>

## <span data-ttu-id="2efb7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2efb7-131">RELATED LINKS</span></span>

[<span data-ttu-id="2efb7-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2efb7-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="2efb7-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="2efb7-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
