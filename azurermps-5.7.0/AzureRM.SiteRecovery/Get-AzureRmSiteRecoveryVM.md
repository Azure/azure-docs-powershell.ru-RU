---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567898"
---
# <span data-ttu-id="0c93d-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="0c93d-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="0c93d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c93d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c93d-103">Получение сведений о виртуальных машинах, управляемых с восстановлением сайта.</span><span class="sxs-lookup"><span data-stu-id="0c93d-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c93d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c93d-104">SYNTAX</span></span>

### <span data-ttu-id="0c93d-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c93d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c93d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0c93d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c93d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0c93d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c93d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c93d-108">DESCRIPTION</span></span>
<span data-ttu-id="0c93d-109">Командлет **Get-AzureRmSiteRecoveryVM** получает сведения о виртуальных машинах, управляемых в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0c93d-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="0c93d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c93d-110">EXAMPLES</span></span>

## <span data-ttu-id="0c93d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c93d-111">PARAMETERS</span></span>

### <span data-ttu-id="0c93d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c93d-112">-DefaultProfile</span></span>
<span data-ttu-id="0c93d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c93d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c93d-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0c93d-114">-FriendlyName</span></span>
<span data-ttu-id="0c93d-115">Указывает понятное имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c93d-115">Specifies the friendly name of the virtual machine.</span></span>

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

### <span data-ttu-id="0c93d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c93d-116">-Name</span></span>
<span data-ttu-id="0c93d-117">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c93d-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0c93d-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0c93d-118">-ProtectionContainer</span></span>
<span data-ttu-id="0c93d-119">Указывает объект контейнера защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="0c93d-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c93d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c93d-120">CommonParameters</span></span>
<span data-ttu-id="0c93d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c93d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c93d-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c93d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c93d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c93d-123">INPUTS</span></span>

### <span data-ttu-id="0c93d-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0c93d-124">ASRProtectionContainer</span></span>
<span data-ttu-id="0c93d-125">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0c93d-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="0c93d-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0c93d-126">ASRProtectionContainer</span></span>
<span data-ttu-id="0c93d-127">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0c93d-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="0c93d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c93d-128">OUTPUTS</span></span>

### <span data-ttu-id="0c93d-129">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="0c93d-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="0c93d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c93d-130">NOTES</span></span>

## <span data-ttu-id="0c93d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c93d-131">RELATED LINKS</span></span>

[<span data-ttu-id="0c93d-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="0c93d-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
