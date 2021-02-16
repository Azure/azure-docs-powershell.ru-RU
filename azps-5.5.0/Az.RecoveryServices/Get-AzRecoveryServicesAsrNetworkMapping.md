---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227105"
---
# <span data-ttu-id="7e844-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e844-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="7e844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e844-102">SYNOPSIS</span></span>
<span data-ttu-id="7e844-103">Получает сведения о сопоставлениях сети восстановления сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="7e844-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="7e844-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e844-104">SYNTAX</span></span>

### <span data-ttu-id="7e844-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e844-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e844-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="7e844-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e844-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e844-107">DESCRIPTION</span></span>
<span data-ttu-id="7e844-108">Командлет **Get-AzRecoveryServicesAsrNetworkMapping** получает сведения о сопоставлениях сети восстановления сайтов Azure для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7e844-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="7e844-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e844-109">EXAMPLES</span></span>

### <span data-ttu-id="7e844-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e844-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="7e844-111">Возвращает все сопоставления сетей для переданной сети.</span><span class="sxs-lookup"><span data-stu-id="7e844-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="7e844-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7e844-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="7e844-113">Возвращает сопоставление сетей с указанным именем в указанной структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="7e844-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="7e844-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e844-114">PARAMETERS</span></span>

### <span data-ttu-id="7e844-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e844-115">-DefaultProfile</span></span>
<span data-ttu-id="7e844-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e844-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7e844-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7e844-117">-Name</span></span>
<span data-ttu-id="7e844-118">Имя объекта сетевого сопоставления ASR, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="7e844-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="7e844-119">-Network</span><span class="sxs-lookup"><span data-stu-id="7e844-119">-Network</span></span>
<span data-ttu-id="7e844-120">Получите сопоставления сетей ASR, соответствующие указанному объекту ASR сети.</span><span class="sxs-lookup"><span data-stu-id="7e844-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="7e844-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7e844-121">-PrimaryFabric</span></span>
<span data-ttu-id="7e844-122">Получите сетевые сопоставления ASR, соответствующие указанному объекту основной тканью.</span><span class="sxs-lookup"><span data-stu-id="7e844-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="7e844-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e844-123">CommonParameters</span></span>
<span data-ttu-id="7e844-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e844-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e844-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e844-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e844-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e844-126">INPUTS</span></span>

### <span data-ttu-id="7e844-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="7e844-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="7e844-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="7e844-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="7e844-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e844-129">OUTPUTS</span></span>

### <span data-ttu-id="7e844-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e844-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="7e844-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e844-131">NOTES</span></span>

## <span data-ttu-id="7e844-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e844-132">RELATED LINKS</span></span>

[<span data-ttu-id="7e844-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e844-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="7e844-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7e844-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
