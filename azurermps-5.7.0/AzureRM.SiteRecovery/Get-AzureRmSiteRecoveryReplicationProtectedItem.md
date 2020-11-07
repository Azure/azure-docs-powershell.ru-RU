---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733980"
---
# <span data-ttu-id="f9efc-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f9efc-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="f9efc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9efc-102">SYNOPSIS</span></span>
<span data-ttu-id="f9efc-103">Возвращает свойства элементов, защищенных с помощью Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9efc-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9efc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9efc-104">SYNTAX</span></span>

### <span data-ttu-id="f9efc-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9efc-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9efc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f9efc-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9efc-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f9efc-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9efc-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="f9efc-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9efc-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9efc-109">DESCRIPTION</span></span>
<span data-ttu-id="f9efc-110">Командлет **Get-AzureRmSiteRecoveryReplicationProtectedItem** получает свойства защищенных элементов восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f9efc-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="f9efc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9efc-111">EXAMPLES</span></span>

## <span data-ttu-id="f9efc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9efc-112">PARAMETERS</span></span>

### <span data-ttu-id="f9efc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9efc-113">-DefaultProfile</span></span>
<span data-ttu-id="f9efc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9efc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9efc-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f9efc-115">-FriendlyName</span></span>
<span data-ttu-id="f9efc-116">Указывает понятное имя для элемента, защищенного репликацией, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f9efc-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9efc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9efc-117">-Name</span></span>
<span data-ttu-id="f9efc-118">Указывает имя защищенного элемента репликации, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f9efc-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9efc-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f9efc-119">-ProtectableItem</span></span>
<span data-ttu-id="f9efc-120">Указывает защищаемый элемент, соответствующий элементу, защищенному репликацией.</span><span class="sxs-lookup"><span data-stu-id="f9efc-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9efc-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f9efc-121">-ProtectionContainer</span></span>
<span data-ttu-id="f9efc-122">Указывает объект контейнера защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f9efc-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9efc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9efc-123">CommonParameters</span></span>
<span data-ttu-id="f9efc-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9efc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9efc-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9efc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9efc-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9efc-126">INPUTS</span></span>

### <span data-ttu-id="f9efc-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="f9efc-127">ASRProtectableItem</span></span>
<span data-ttu-id="f9efc-128">Параметр "ProtectableItem" принимает значение типа "ASRProtectableItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f9efc-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="f9efc-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f9efc-129">ASRProtectionContainer</span></span>
<span data-ttu-id="f9efc-130">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f9efc-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="f9efc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9efc-131">OUTPUTS</span></span>

### <span data-ttu-id="f9efc-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRReplicationProtectedItem, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="f9efc-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f9efc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9efc-133">NOTES</span></span>

## <span data-ttu-id="f9efc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9efc-134">RELATED LINKS</span></span>

[<span data-ttu-id="f9efc-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f9efc-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="f9efc-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f9efc-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="f9efc-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f9efc-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
