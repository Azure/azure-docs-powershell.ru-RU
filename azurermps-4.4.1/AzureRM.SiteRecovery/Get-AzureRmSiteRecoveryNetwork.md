---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562104"
---
# <span data-ttu-id="121b1-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="121b1-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="121b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="121b1-102">SYNOPSIS</span></span>
<span data-ttu-id="121b1-103">Возвращает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="121b1-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="121b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="121b1-104">SYNTAX</span></span>

### <span data-ttu-id="121b1-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="121b1-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="121b1-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="121b1-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="121b1-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="121b1-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="121b1-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="121b1-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="121b1-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="121b1-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="121b1-110">ByName</span><span class="sxs-lookup"><span data-stu-id="121b1-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="121b1-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="121b1-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="121b1-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="121b1-112">DESCRIPTION</span></span>
<span data-ttu-id="121b1-113">Командлет **Get-AzureRmSiteRecoveryNetwork** получает сведения об сетях Azure Site Recovery для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="121b1-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="121b1-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="121b1-114">EXAMPLES</span></span>

## <span data-ttu-id="121b1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="121b1-115">PARAMETERS</span></span>

### <span data-ttu-id="121b1-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="121b1-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121b1-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="121b1-117">-FriendlyName</span></span>
<span data-ttu-id="121b1-118">Указывает понятное имя сети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="121b1-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121b1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="121b1-119">-Name</span></span>
<span data-ttu-id="121b1-120">Указывает имя сети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="121b1-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121b1-121">-Сервер</span><span class="sxs-lookup"><span data-stu-id="121b1-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="121b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="121b1-122">-DefaultProfile</span></span>
<span data-ttu-id="121b1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="121b1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="121b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="121b1-124">CommonParameters</span></span>
<span data-ttu-id="121b1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="121b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="121b1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="121b1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="121b1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="121b1-127">INPUTS</span></span>

### <span data-ttu-id="121b1-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="121b1-128">ASRFabric</span></span>
<span data-ttu-id="121b1-129">Параметр "Fabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="121b1-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="121b1-130">Подстрок</span><span class="sxs-lookup"><span data-stu-id="121b1-130">String</span></span>
<span data-ttu-id="121b1-131">Параметр "FriendlyName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="121b1-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="121b1-132">Подстрок</span><span class="sxs-lookup"><span data-stu-id="121b1-132">String</span></span>
<span data-ttu-id="121b1-133">Параметр "FriendlyName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="121b1-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="121b1-134">Подстрок</span><span class="sxs-lookup"><span data-stu-id="121b1-134">String</span></span>
<span data-ttu-id="121b1-135">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="121b1-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="121b1-136">Подстрок</span><span class="sxs-lookup"><span data-stu-id="121b1-136">String</span></span>
<span data-ttu-id="121b1-137">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="121b1-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="121b1-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="121b1-138">ASRServer</span></span>
<span data-ttu-id="121b1-139">Параметр Server принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="121b1-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="121b1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="121b1-140">OUTPUTS</span></span>

### <span data-ttu-id="121b1-141">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="121b1-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="121b1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="121b1-142">NOTES</span></span>

## <span data-ttu-id="121b1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="121b1-143">RELATED LINKS</span></span>

