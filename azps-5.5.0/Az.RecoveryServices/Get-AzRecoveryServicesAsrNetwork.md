---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236132"
---
# <span data-ttu-id="2712a-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="2712a-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="2712a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2712a-102">SYNOPSIS</span></span>
<span data-ttu-id="2712a-103">Получает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2712a-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="2712a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2712a-104">SYNTAX</span></span>

### <span data-ttu-id="2712a-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2712a-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2712a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2712a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2712a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2712a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2712a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2712a-108">DESCRIPTION</span></span>
<span data-ttu-id="2712a-109">Командлет **Get-AzRecoveryServicesAsrNetwork** получает сведения о сетях восстановления сайтов Azure для текущего хранилища восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="2712a-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="2712a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2712a-110">EXAMPLES</span></span>

### <span data-ttu-id="2712a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2712a-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="2712a-112">Все известные сети в указанном материале.</span><span class="sxs-lookup"><span data-stu-id="2712a-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="2712a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2712a-113">PARAMETERS</span></span>

### <span data-ttu-id="2712a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2712a-114">-DefaultProfile</span></span>
<span data-ttu-id="2712a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2712a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2712a-116">-Ткань</span><span class="sxs-lookup"><span data-stu-id="2712a-116">-Fabric</span></span>
<span data-ttu-id="2712a-117">Объект asR fabric object</span><span class="sxs-lookup"><span data-stu-id="2712a-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2712a-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2712a-118">-FriendlyName</span></span>
<span data-ttu-id="2712a-119">Имя объекта ASR сети.</span><span class="sxs-lookup"><span data-stu-id="2712a-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2712a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2712a-120">-Name</span></span>
<span data-ttu-id="2712a-121">Имя объекта ASR сети.</span><span class="sxs-lookup"><span data-stu-id="2712a-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="2712a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2712a-122">CommonParameters</span></span>
<span data-ttu-id="2712a-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2712a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2712a-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2712a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2712a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2712a-125">INPUTS</span></span>

### <span data-ttu-id="2712a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2712a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="2712a-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2712a-127">OUTPUTS</span></span>

### <span data-ttu-id="2712a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="2712a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="2712a-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2712a-129">NOTES</span></span>

## <span data-ttu-id="2712a-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2712a-130">RELATED LINKS</span></span>
