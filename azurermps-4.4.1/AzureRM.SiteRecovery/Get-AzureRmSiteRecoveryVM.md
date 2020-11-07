---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732685"
---
# <span data-ttu-id="cf06e-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="cf06e-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="cf06e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf06e-102">SYNOPSIS</span></span>
<span data-ttu-id="cf06e-103">Получение сведений о виртуальных машинах, управляемых с восстановлением сайта.</span><span class="sxs-lookup"><span data-stu-id="cf06e-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf06e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf06e-104">SYNTAX</span></span>

### <span data-ttu-id="cf06e-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf06e-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf06e-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="cf06e-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf06e-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf06e-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf06e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf06e-108">DESCRIPTION</span></span>
<span data-ttu-id="cf06e-109">Командлет **Get-AzureRmSiteRecoveryVM** получает сведения о виртуальных машинах, управляемых в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cf06e-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="cf06e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf06e-110">EXAMPLES</span></span>

## <span data-ttu-id="cf06e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf06e-111">PARAMETERS</span></span>

### <span data-ttu-id="cf06e-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cf06e-112">-FriendlyName</span></span>
<span data-ttu-id="cf06e-113">Указывает понятное имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf06e-113">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="cf06e-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf06e-114">-Name</span></span>
<span data-ttu-id="cf06e-115">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf06e-115">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="cf06e-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cf06e-116">-ProtectionContainer</span></span>
<span data-ttu-id="cf06e-117">Указывает объект контейнера защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="cf06e-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf06e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf06e-118">-DefaultProfile</span></span>
<span data-ttu-id="cf06e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf06e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf06e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf06e-120">CommonParameters</span></span>
<span data-ttu-id="cf06e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf06e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf06e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf06e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf06e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf06e-123">INPUTS</span></span>

### <span data-ttu-id="cf06e-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cf06e-124">ASRProtectionContainer</span></span>
<span data-ttu-id="cf06e-125">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cf06e-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="cf06e-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cf06e-126">ASRProtectionContainer</span></span>
<span data-ttu-id="cf06e-127">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cf06e-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="cf06e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf06e-128">OUTPUTS</span></span>

### <span data-ttu-id="cf06e-129">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="cf06e-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="cf06e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf06e-130">NOTES</span></span>

## <span data-ttu-id="cf06e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf06e-131">RELATED LINKS</span></span>

[<span data-ttu-id="cf06e-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="cf06e-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
