---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: 6eec8f849d555fd2bf71f564c2e5c3ed9c699d80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978803"
---
# <span data-ttu-id="9cd89-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="9cd89-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="9cd89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd89-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd89-103">Создание в памяти объекта для CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9cd89-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9cd89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9cd89-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="9cd89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cd89-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd89-106">Создание в памяти объекта для CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9cd89-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9cd89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9cd89-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd89-108">Пример 1. Создание объекта свойств профиля роли</span><span class="sxs-lookup"><span data-stu-id="9cd89-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="9cd89-109">Эта команда создает объект свойств профиля роли, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="9cd89-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="9cd89-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="9cd89-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="9cd89-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cd89-111">PARAMETERS</span></span>

### <span data-ttu-id="9cd89-112">-Name</span><span class="sxs-lookup"><span data-stu-id="9cd89-112">-Name</span></span>
<span data-ttu-id="9cd89-113">Имя профиля роли.</span><span class="sxs-lookup"><span data-stu-id="9cd89-113">Name of role profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd89-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9cd89-114">-SkuCapacity</span></span>
<span data-ttu-id="9cd89-115">Количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="9cd89-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd89-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9cd89-116">-SkuName</span></span>
<span data-ttu-id="9cd89-117">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="9cd89-117">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd89-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9cd89-118">-SkuTier</span></span>
<span data-ttu-id="9cd89-119">SKUTier.</span><span class="sxs-lookup"><span data-stu-id="9cd89-119">SkuTier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd89-120">CommonParameters</span></span>
<span data-ttu-id="9cd89-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd89-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cd89-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd89-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cd89-123">INPUTS</span></span>

## <span data-ttu-id="9cd89-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9cd89-124">OUTPUTS</span></span>

### <span data-ttu-id="9cd89-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9cd89-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9cd89-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9cd89-126">NOTES</span></span>

<span data-ttu-id="9cd89-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9cd89-127">ALIASES</span></span>

## <span data-ttu-id="9cd89-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cd89-128">RELATED LINKS</span></span>

