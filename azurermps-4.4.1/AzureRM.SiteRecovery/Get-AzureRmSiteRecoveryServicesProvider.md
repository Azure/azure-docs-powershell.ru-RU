---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e61136122873f7837120065194252aba145ea733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568292"
---
# <span data-ttu-id="25da3-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25da3-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="25da3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25da3-102">SYNOPSIS</span></span>
<span data-ttu-id="25da3-103">Возвращает сведения о поставщиках Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="25da3-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25da3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25da3-104">SYNTAX</span></span>

### <span data-ttu-id="25da3-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25da3-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25da3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="25da3-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25da3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="25da3-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25da3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25da3-108">DESCRIPTION</span></span>
<span data-ttu-id="25da3-109">Командлет **Get-AzureRmSiteRecoveryServicesProvider** получает сведения о поставщиках Azure Site Recovery в хранилище.</span><span class="sxs-lookup"><span data-stu-id="25da3-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="25da3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25da3-110">EXAMPLES</span></span>

## <span data-ttu-id="25da3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25da3-111">PARAMETERS</span></span>

### <span data-ttu-id="25da3-112">-Fabric</span><span class="sxs-lookup"><span data-stu-id="25da3-112">-Fabric</span></span>
<span data-ttu-id="25da3-113">Указывает объект структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="25da3-113">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25da3-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="25da3-114">-FriendlyName</span></span>
<span data-ttu-id="25da3-115">Указывает понятное имя поставщика Azure Site Recovery, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25da3-115">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25da3-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25da3-116">-Name</span></span>
<span data-ttu-id="25da3-117">Указывает имя поставщика Azure Site Recovery, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25da3-117">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="25da3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25da3-118">-DefaultProfile</span></span>
<span data-ttu-id="25da3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25da3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25da3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25da3-120">CommonParameters</span></span>
<span data-ttu-id="25da3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25da3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25da3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25da3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25da3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25da3-123">INPUTS</span></span>

### <span data-ttu-id="25da3-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="25da3-124">ASRFabric</span></span>
<span data-ttu-id="25da3-125">Параметр "Fabric" принимает значение типа "ASRFabric" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="25da3-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="25da3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25da3-126">OUTPUTS</span></span>

### <span data-ttu-id="25da3-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="25da3-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="25da3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="25da3-128">NOTES</span></span>

## <span data-ttu-id="25da3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25da3-129">RELATED LINKS</span></span>

[<span data-ttu-id="25da3-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25da3-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="25da3-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="25da3-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
