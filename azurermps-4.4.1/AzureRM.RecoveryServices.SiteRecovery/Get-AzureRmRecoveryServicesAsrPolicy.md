---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569259"
---
# <span data-ttu-id="9215a-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9215a-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="9215a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9215a-102">SYNOPSIS</span></span>
<span data-ttu-id="9215a-103">Возвращает политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="9215a-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9215a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9215a-104">SYNTAX</span></span>

### <span data-ttu-id="9215a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9215a-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="9215a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9215a-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="9215a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9215a-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="9215a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9215a-108">DESCRIPTION</span></span>
<span data-ttu-id="9215a-109">Командлет **Get-AzureRmRecoveryServicesAsrPolicy** получает список настроенных политик репликации для Azure Site Recovery или определенную политику репликации по имени.</span><span class="sxs-lookup"><span data-stu-id="9215a-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="9215a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9215a-110">EXAMPLES</span></span>

### <span data-ttu-id="9215a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9215a-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="9215a-112">Retruns политику репликации с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="9215a-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="9215a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9215a-113">PARAMETERS</span></span>

### <span data-ttu-id="9215a-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9215a-114">-FriendlyName</span></span>
<span data-ttu-id="9215a-115">Указывает понятное имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="9215a-115">Specifies the friendly name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="9215a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9215a-116">-Name</span></span>
<span data-ttu-id="9215a-117">Задает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="9215a-117">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="9215a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9215a-118">CommonParameters</span></span>
<span data-ttu-id="9215a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9215a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9215a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9215a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9215a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9215a-121">INPUTS</span></span>

### <span data-ttu-id="9215a-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="9215a-122">None</span></span>

## <span data-ttu-id="9215a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9215a-123">OUTPUTS</span></span>

### <span data-ttu-id="9215a-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9215a-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9215a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="9215a-125">NOTES</span></span>

## <span data-ttu-id="9215a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9215a-126">RELATED LINKS</span></span>

[<span data-ttu-id="9215a-127">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9215a-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="9215a-128">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="9215a-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
