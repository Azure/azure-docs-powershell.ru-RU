---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559579"
---
# <span data-ttu-id="6f3c4-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6f3c4-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="6f3c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3c4-103">Получение сведений о структуре восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f3c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f3c4-104">SYNTAX</span></span>

### <span data-ttu-id="6f3c4-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f3c4-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="6f3c4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f3c4-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="6f3c4-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6f3c4-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="6f3c4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f3c4-108">DESCRIPTION</span></span>
<span data-ttu-id="6f3c4-109">Командлет **Get-AzureRmRecoveryServicesAsrFabric** получает свойства указанной структуры восстановления сайта Azure или всех структур восстановления сайта Azure в хранилище службы восстановления.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="6f3c4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f3c4-110">EXAMPLES</span></span>

### <span data-ttu-id="6f3c4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f3c4-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="6f3c4-112">Возвращает все структуры восстановления сайта Azure в хранилище.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="6f3c4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f3c4-113">PARAMETERS</span></span>

### <span data-ttu-id="6f3c4-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6f3c4-114">-FriendlyName</span></span>
<span data-ttu-id="6f3c4-115">Найдите структуру ASR с помощью понятного имени структуры.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="6f3c4-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f3c4-116">-Name</span></span>
<span data-ttu-id="6f3c4-117">Найдите структуру ASR с помощью имени структуры.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-117">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="6f3c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3c4-118">CommonParameters</span></span>
<span data-ttu-id="6f3c4-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f3c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3c4-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f3c4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3c4-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f3c4-121">INPUTS</span></span>

### <span data-ttu-id="6f3c4-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f3c4-122">None</span></span>

## <span data-ttu-id="6f3c4-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f3c4-123">OUTPUTS</span></span>

### <span data-ttu-id="6f3c4-124">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="6f3c4-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6f3c4-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f3c4-125">NOTES</span></span>

## <span data-ttu-id="6f3c4-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f3c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="6f3c4-127">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6f3c4-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="6f3c4-128">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="6f3c4-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
