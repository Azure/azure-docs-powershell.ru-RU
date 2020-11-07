---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 48437526fdaf8ae226ff7693b417fcff7ffc93d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904949"
---
# <span data-ttu-id="4ffcc-101">Get-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="4ffcc-101">Get-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="4ffcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ffcc-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffcc-103">Получение подробных сведений о серверах vCenter, зарегистрированных для обнаружения на сервере конфигурации, указанном в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-103">Gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="4ffcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ffcc-104">SYNTAX</span></span>

### <span data-ttu-id="4ffcc-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ffcc-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ffcc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffcc-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ffcc-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4ffcc-107">ByName</span></span>
```
Get-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ffcc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffcc-108">DESCRIPTION</span></span>
<span data-ttu-id="4ffcc-109">Командлет **Get-AzRecoveryServicesAsrvCenter** получает сведения о серверах vCenter Server, зарегистрированных для обнаружения на сервере конфигурации, указанном в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-109">The **Get-AzRecoveryServicesAsrvCenter** cmdlet gets details of the vCenter servers registered for discovery on the Configuration server specified by the ASR fabric.</span></span>

## <span data-ttu-id="4ffcc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffcc-110">EXAMPLES</span></span>

### <span data-ttu-id="4ffcc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ffcc-111">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric -Name $Name

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

<span data-ttu-id="4ffcc-112">Скачайте службу восстановления сайта Azure vCenter по имени и названию vCenter.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-112">Get azure site recovery vCenter by fabric name and name of vCenter.</span></span>

### <span data-ttu-id="4ffcc-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4ffcc-113">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrvCenter -Fabric $Fabric
```

<span data-ttu-id="4ffcc-114">Получите список vCenter Site Recovery для Azure по имени структуры.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-114">Get azure site recovery vCenter list by fabric name.</span></span>

## <span data-ttu-id="4ffcc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ffcc-115">PARAMETERS</span></span>

### <span data-ttu-id="4ffcc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffcc-116">-DefaultProfile</span></span>
<span data-ttu-id="4ffcc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ffcc-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4ffcc-118">-Fabric</span></span>
<span data-ttu-id="4ffcc-119">Объект Fabric ASR, представляющий сервер конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-119">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="4ffcc-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ffcc-120">-Name</span></span>
<span data-ttu-id="4ffcc-121">Имя сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-121">Name of the vCenter server.</span></span>

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

### <span data-ttu-id="4ffcc-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ffcc-122">-ResourceId</span></span>
<span data-ttu-id="4ffcc-123">Указывает resourceId для vCenter.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-123">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="4ffcc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffcc-124">CommonParameters</span></span>
<span data-ttu-id="4ffcc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ffcc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffcc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffcc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffcc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ffcc-127">INPUTS</span></span>

### <span data-ttu-id="4ffcc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4ffcc-128">System.String</span></span>

### <span data-ttu-id="4ffcc-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4ffcc-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4ffcc-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffcc-130">OUTPUTS</span></span>

### <span data-ttu-id="4ffcc-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="4ffcc-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="4ffcc-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ffcc-132">NOTES</span></span>

## <span data-ttu-id="4ffcc-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ffcc-133">RELATED LINKS</span></span>
