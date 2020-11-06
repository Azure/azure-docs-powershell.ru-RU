---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 8db3dd9579e528110ec41f59b1c29da5d132d18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568166"
---
# <span data-ttu-id="de33f-101">Get-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="de33f-101">Get-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="de33f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de33f-102">SYNOPSIS</span></span>
<span data-ttu-id="de33f-103">Получение подробных сведений о серверах vCenter, зарегистрированных для обнаружения на сервере конфигурации, указанном в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="de33f-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de33f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de33f-104">SYNTAX</span></span>

### <span data-ttu-id="de33f-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de33f-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de33f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de33f-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de33f-107">ByName</span><span class="sxs-lookup"><span data-stu-id="de33f-107">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de33f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de33f-108">DESCRIPTION</span></span>
<span data-ttu-id="de33f-109">Командлет **Get-AzureRmRecoveryServicesAsrvCenter** получает сведения о серверах vCenter Server, зарегистрированных для обнаружения на сервере конфигурации, указанном в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="de33f-109">The **Get-AzureRmRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="de33f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de33f-110">EXAMPLES</span></span>

### <span data-ttu-id="de33f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de33f-111">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

FriendlyName          : inmtest81
Server                : 10.150.209.27
Port                  : 443
Name                  : inmtest81
ID                    : /Subscriptions/xxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxx/replicationFabrics/xxxxxxxxxxxxxxxxx/replicationvCenters/inmtest81
FabricArmResourceName : d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9
ProcessServerId       : 526C9B6C-4039-D841-97A92FB0BD153B53
AccountId             : 2
DiscoveryStatus       : Pending
LastHeartbeat         :
```

<span data-ttu-id="de33f-112">Скачайте службу восстановления сайта Azure vCenter по имени и названию vCenter.</span><span class="sxs-lookup"><span data-stu-id="de33f-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="de33f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="de33f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="de33f-114">Получите список vCenter Site Recovery для Azure по имени структуры.</span><span class="sxs-lookup"><span data-stu-id="de33f-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="de33f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de33f-115">PARAMETERS</span></span>

### <span data-ttu-id="de33f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de33f-116">-DefaultProfile</span></span>
<span data-ttu-id="de33f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de33f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de33f-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="de33f-118">-Fabric</span></span>
<span data-ttu-id="de33f-119">Объект Fabric ASR, представляющий сервер конфигурации.</span><span class="sxs-lookup"><span data-stu-id="de33f-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de33f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de33f-120">-Name</span></span>
<span data-ttu-id="de33f-121">Имя сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="de33f-121">Name of the vCenter server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de33f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de33f-122">-ResourceId</span></span>
<span data-ttu-id="de33f-123">Указывает resourceId для vCenter.</span><span class="sxs-lookup"><span data-stu-id="de33f-123">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de33f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de33f-124">CommonParameters</span></span>
<span data-ttu-id="de33f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de33f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de33f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de33f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de33f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de33f-127">INPUTS</span></span>

### <span data-ttu-id="de33f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="de33f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="de33f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de33f-129">OUTPUTS</span></span>

### <span data-ttu-id="de33f-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="de33f-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de33f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="de33f-131">NOTES</span></span>

## <span data-ttu-id="de33f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de33f-132">RELATED LINKS</span></span>
