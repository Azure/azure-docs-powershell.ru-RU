---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 34977acc0889a3fa557af7dfc9f02d6937e22fde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561627"
---
# <span data-ttu-id="41621-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="41621-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="41621-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41621-102">SYNOPSIS</span></span>
<span data-ttu-id="41621-103">Возвращает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="41621-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41621-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41621-104">SYNTAX</span></span>

### <span data-ttu-id="41621-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41621-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41621-106">ByName</span><span class="sxs-lookup"><span data-stu-id="41621-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41621-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="41621-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41621-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41621-108">DESCRIPTION</span></span>
<span data-ttu-id="41621-109">Командлет **Get-AzureRmRecoveryServicesAsrNetwork** получает сведения об сетях Azure Site Recovery для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="41621-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="41621-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41621-110">EXAMPLES</span></span>

### <span data-ttu-id="41621-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41621-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="41621-112">Возвращает все известные сети в указанной структуре.</span><span class="sxs-lookup"><span data-stu-id="41621-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="41621-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41621-113">PARAMETERS</span></span>

### <span data-ttu-id="41621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41621-114">-DefaultProfile</span></span>
<span data-ttu-id="41621-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41621-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="41621-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="41621-116">-Fabric</span></span>
<span data-ttu-id="41621-117">Объект фабрики ASR</span><span class="sxs-lookup"><span data-stu-id="41621-117">ASR fabric object</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41621-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="41621-118">-FriendlyName</span></span>
<span data-ttu-id="41621-119">Понятное имя объекта сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="41621-119">Friendly name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41621-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41621-120">-Name</span></span>
<span data-ttu-id="41621-121">Имя объекта сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="41621-121">Name of network ASR object.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41621-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41621-122">CommonParameters</span></span>
<span data-ttu-id="41621-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41621-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41621-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41621-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41621-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41621-125">INPUTS</span></span>

### <span data-ttu-id="41621-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="41621-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="41621-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41621-127">OUTPUTS</span></span>

### <span data-ttu-id="41621-128">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="41621-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="41621-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="41621-129">NOTES</span></span>

## <span data-ttu-id="41621-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41621-130">RELATED LINKS</span></span>
