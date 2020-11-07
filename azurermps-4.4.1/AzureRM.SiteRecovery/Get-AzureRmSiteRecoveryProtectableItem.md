---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 0b2fe8f500e17bc21407870a712ad4b9f00fd544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732400"
---
# <span data-ttu-id="b1816-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b1816-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="b1816-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1816-102">SYNOPSIS</span></span>
<span data-ttu-id="b1816-103">Получите доступ к защищенным элементам в контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="b1816-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1816-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1816-104">SYNTAX</span></span>

### <span data-ttu-id="b1816-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1816-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1816-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b1816-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1816-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b1816-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1816-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1816-108">DESCRIPTION</span></span>
<span data-ttu-id="b1816-109">Командлет **Get-AzureRmSiteRecoveryProtectableItem** получает защищенные элементы в контейнере защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1816-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="b1816-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1816-110">EXAMPLES</span></span>

## <span data-ttu-id="b1816-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1816-111">PARAMETERS</span></span>

### <span data-ttu-id="b1816-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b1816-112">-FriendlyName</span></span>
<span data-ttu-id="b1816-113">Указывает понятное имя защищенного элемента Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1816-113">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1816-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b1816-114">-Name</span></span>
<span data-ttu-id="b1816-115">Указывает имя защищенного элемента Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1816-115">Specifies the name of the Azure Site Recovery protectable item.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1816-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b1816-116">-ProtectionContainer</span></span>
<span data-ttu-id="b1816-117">Указывает объект контейнера защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b1816-117">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1816-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1816-118">-DefaultProfile</span></span>
<span data-ttu-id="b1816-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1816-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1816-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1816-120">CommonParameters</span></span>
<span data-ttu-id="b1816-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1816-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1816-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1816-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1816-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1816-123">INPUTS</span></span>

### <span data-ttu-id="b1816-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b1816-124">ASRProtectionContainer</span></span>
<span data-ttu-id="b1816-125">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b1816-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="b1816-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1816-126">OUTPUTS</span></span>

### <span data-ttu-id="b1816-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="b1816-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b1816-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1816-128">NOTES</span></span>

## <span data-ttu-id="b1816-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1816-129">RELATED LINKS</span></span>

[<span data-ttu-id="b1816-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b1816-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="b1816-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b1816-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
