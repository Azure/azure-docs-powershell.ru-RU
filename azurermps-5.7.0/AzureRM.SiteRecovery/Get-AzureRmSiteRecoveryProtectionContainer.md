---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733984"
---
# <span data-ttu-id="4e274-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4e274-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="4e274-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e274-102">SYNOPSIS</span></span>
<span data-ttu-id="4e274-103">Получает контейнеры защиты для текущего хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="4e274-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e274-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e274-104">SYNTAX</span></span>

### <span data-ttu-id="4e274-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e274-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e274-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4e274-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e274-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="4e274-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e274-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4e274-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e274-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="4e274-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e274-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="4e274-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e274-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e274-111">DESCRIPTION</span></span>
<span data-ttu-id="4e274-112">Командлет **Get-AzureRmSiteRecoveryProtectionContainer** получает контейнеры защиты для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="4e274-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="4e274-113">Контейнер защиты — это логический контейнер для защищенных объектов, таких как виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="4e274-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="4e274-114">Политики защиты определяют параметры репликации для защищенных элементов и могут быть связаны с контейнером защиты и применяются к защищенному объекту.</span><span class="sxs-lookup"><span data-stu-id="4e274-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="4e274-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e274-115">EXAMPLES</span></span>

## <span data-ttu-id="4e274-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e274-116">PARAMETERS</span></span>

### <span data-ttu-id="4e274-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e274-117">-DefaultProfile</span></span>
<span data-ttu-id="4e274-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e274-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e274-119">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4e274-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e274-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4e274-120">-FriendlyName</span></span>
<span data-ttu-id="4e274-121">Указывает понятное имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="4e274-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e274-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e274-122">-Name</span></span>
<span data-ttu-id="4e274-123">Указывает имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="4e274-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e274-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e274-124">CommonParameters</span></span>
<span data-ttu-id="4e274-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e274-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e274-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e274-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e274-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e274-127">INPUTS</span></span>

### <span data-ttu-id="4e274-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4e274-128">ASRFabric</span></span>
<span data-ttu-id="4e274-129">Параметр "Fabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4e274-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="4e274-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e274-130">OUTPUTS</span></span>

### <span data-ttu-id="4e274-131">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="4e274-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="4e274-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e274-132">NOTES</span></span>

## <span data-ttu-id="4e274-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e274-133">RELATED LINKS</span></span>

