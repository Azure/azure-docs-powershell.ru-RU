---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249844"
---
# <span data-ttu-id="b1dec-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="b1dec-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="b1dec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1dec-102">SYNOPSIS</span></span>
<span data-ttu-id="b1dec-103">Возвращает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b1dec-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="b1dec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1dec-104">SYNTAX</span></span>

### <span data-ttu-id="b1dec-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1dec-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1dec-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b1dec-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b1dec-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b1dec-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1dec-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1dec-108">DESCRIPTION</span></span>
<span data-ttu-id="b1dec-109">Командлет **Get-AzRecoveryServicesAsrNetwork** получает сведения об сетях Azure Site Recovery для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1dec-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b1dec-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1dec-110">EXAMPLES</span></span>

### <span data-ttu-id="b1dec-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1dec-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="b1dec-112">Возвращает все известные сети в указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="b1dec-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="b1dec-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1dec-113">PARAMETERS</span></span>

### <span data-ttu-id="b1dec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1dec-114">-DefaultProfile</span></span>
<span data-ttu-id="b1dec-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1dec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b1dec-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="b1dec-116">-Fabric</span></span>
<span data-ttu-id="b1dec-117">Объект фабрики ASR</span><span class="sxs-lookup"><span data-stu-id="b1dec-117">ASR fabric object</span></span>

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

### <span data-ttu-id="b1dec-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b1dec-118">-FriendlyName</span></span>
<span data-ttu-id="b1dec-119">Понятное имя объекта сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="b1dec-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="b1dec-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1dec-120">-Name</span></span>
<span data-ttu-id="b1dec-121">Имя объекта сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="b1dec-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="b1dec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1dec-122">CommonParameters</span></span>
<span data-ttu-id="b1dec-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1dec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1dec-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1dec-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1dec-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1dec-125">INPUTS</span></span>

### <span data-ttu-id="b1dec-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b1dec-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b1dec-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1dec-127">OUTPUTS</span></span>

### <span data-ttu-id="b1dec-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="b1dec-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="b1dec-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1dec-129">NOTES</span></span>

## <span data-ttu-id="b1dec-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1dec-130">RELATED LINKS</span></span>
