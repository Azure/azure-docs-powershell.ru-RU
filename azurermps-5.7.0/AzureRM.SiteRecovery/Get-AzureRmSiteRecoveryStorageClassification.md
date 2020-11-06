---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567901"
---
# <span data-ttu-id="ff5cc-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ff5cc-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="ff5cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5cc-103">Возвращает классификации хранилища в восстановлении сайта.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff5cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff5cc-104">SYNTAX</span></span>

### <span data-ttu-id="ff5cc-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff5cc-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff5cc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ff5cc-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff5cc-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ff5cc-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff5cc-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="ff5cc-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff5cc-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="ff5cc-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff5cc-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff5cc-110">DESCRIPTION</span></span>
<span data-ttu-id="ff5cc-111">Командлет **Get-AzureRmSiteRecoveryStorageClassification** возвращает классификацию хранилища в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="ff5cc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff5cc-112">EXAMPLES</span></span>

## <span data-ttu-id="ff5cc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff5cc-113">PARAMETERS</span></span>

### <span data-ttu-id="ff5cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5cc-114">-DefaultProfile</span></span>
<span data-ttu-id="ff5cc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff5cc-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="ff5cc-116">-Fabric</span></span>
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

### <span data-ttu-id="ff5cc-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ff5cc-117">-FriendlyName</span></span>
<span data-ttu-id="ff5cc-118">Указывает понятное имя для классификации хранилища, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ff5cc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff5cc-119">-Name</span></span>
<span data-ttu-id="ff5cc-120">Указывает имя классификации хранилища, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ff5cc-121">-Сервер</span><span class="sxs-lookup"><span data-stu-id="ff5cc-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff5cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5cc-122">CommonParameters</span></span>
<span data-ttu-id="ff5cc-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5cc-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5cc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5cc-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff5cc-125">INPUTS</span></span>

### <span data-ttu-id="ff5cc-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ff5cc-126">ASRFabric</span></span>
<span data-ttu-id="ff5cc-127">Параметр "Fabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="ff5cc-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="ff5cc-128">ASRServer</span></span>
<span data-ttu-id="ff5cc-129">Параметр Server принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ff5cc-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="ff5cc-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff5cc-130">OUTPUTS</span></span>

### <span data-ttu-id="ff5cc-131">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="ff5cc-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="ff5cc-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff5cc-132">NOTES</span></span>

## <span data-ttu-id="ff5cc-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff5cc-133">RELATED LINKS</span></span>

