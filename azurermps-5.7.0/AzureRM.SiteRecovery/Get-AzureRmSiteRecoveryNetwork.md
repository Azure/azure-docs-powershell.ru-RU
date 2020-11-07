---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverynetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 6ffd3a295ecc228ec395a00ba597f2d7b0967a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732511"
---
# <span data-ttu-id="e5c8c-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="e5c8c-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="e5c8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c8c-103">Возвращает сведения о сетях, управляемых восстановлением сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5c8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5c8c-104">SYNTAX</span></span>

### <span data-ttu-id="e5c8c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e5c8c-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c8c-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="e5c8c-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c8c-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="e5c8c-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c8c-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="e5c8c-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5c8c-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="e5c8c-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c8c-110">ByName</span><span class="sxs-lookup"><span data-stu-id="e5c8c-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5c8c-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5c8c-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5c8c-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c8c-112">DESCRIPTION</span></span>
<span data-ttu-id="e5c8c-113">Командлет **Get-AzureRmSiteRecoveryNetwork** получает сведения об сетях Azure Site Recovery для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e5c8c-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5c8c-114">EXAMPLES</span></span>

## <span data-ttu-id="e5c8c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5c8c-115">PARAMETERS</span></span>

### <span data-ttu-id="e5c8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c8c-116">-DefaultProfile</span></span>
<span data-ttu-id="e5c8c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5c8c-118">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e5c8c-118">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c8c-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5c8c-119">-FriendlyName</span></span>
<span data-ttu-id="e5c8c-120">Указывает понятное имя сети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-120">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c8c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5c8c-121">-Name</span></span>
<span data-ttu-id="e5c8c-122">Указывает имя сети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-122">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c8c-123">-Сервер</span><span class="sxs-lookup"><span data-stu-id="e5c8c-123">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c8c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c8c-124">CommonParameters</span></span>
<span data-ttu-id="e5c8c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c8c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5c8c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c8c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5c8c-127">INPUTS</span></span>

### <span data-ttu-id="e5c8c-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e5c8c-128">ASRFabric</span></span>
<span data-ttu-id="e5c8c-129">Параметр "Fabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="e5c8c-130">Подстрок</span><span class="sxs-lookup"><span data-stu-id="e5c8c-130">String</span></span>
<span data-ttu-id="e5c8c-131">Параметр "FriendlyName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e5c8c-132">Подстрок</span><span class="sxs-lookup"><span data-stu-id="e5c8c-132">String</span></span>
<span data-ttu-id="e5c8c-133">Параметр "FriendlyName" принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e5c8c-134">Подстрок</span><span class="sxs-lookup"><span data-stu-id="e5c8c-134">String</span></span>
<span data-ttu-id="e5c8c-135">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e5c8c-136">Подстрок</span><span class="sxs-lookup"><span data-stu-id="e5c8c-136">String</span></span>
<span data-ttu-id="e5c8c-137">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="e5c8c-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="e5c8c-138">ASRServer</span></span>
<span data-ttu-id="e5c8c-139">Параметр Server принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e5c8c-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="e5c8c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5c8c-140">OUTPUTS</span></span>

### <span data-ttu-id="e5c8c-141">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="e5c8c-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="e5c8c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5c8c-142">NOTES</span></span>

## <span data-ttu-id="e5c8c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5c8c-143">RELATED LINKS</span></span>

