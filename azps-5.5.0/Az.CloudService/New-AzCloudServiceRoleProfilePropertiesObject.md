---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215857"
---
# <span data-ttu-id="fb432-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="fb432-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="fb432-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb432-102">SYNOPSIS</span></span>
<span data-ttu-id="fb432-103">Создание объекта в памяти для CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="fb432-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="fb432-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb432-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="fb432-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb432-105">DESCRIPTION</span></span>
<span data-ttu-id="fb432-106">Создание объекта в памяти для CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="fb432-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="fb432-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb432-107">EXAMPLES</span></span>

### <span data-ttu-id="fb432-108">Пример 1. Создание объекта свойств профиля роли</span><span class="sxs-lookup"><span data-stu-id="fb432-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="fb432-109">Эта команда создает объект свойств профиля роли, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="fb432-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="fb432-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="fb432-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="fb432-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb432-111">PARAMETERS</span></span>

### <span data-ttu-id="fb432-112">-Name</span><span class="sxs-lookup"><span data-stu-id="fb432-112">-Name</span></span>
<span data-ttu-id="fb432-113">Имя профиля роли.</span><span class="sxs-lookup"><span data-stu-id="fb432-113">Name of role profile.</span></span>

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

### <span data-ttu-id="fb432-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fb432-114">-SkuCapacity</span></span>
<span data-ttu-id="fb432-115">Количество экземпляров ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="fb432-115">Specifies the number of role instances in the cloud service.</span></span>

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

### <span data-ttu-id="fb432-116">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fb432-116">-SkuName</span></span>
<span data-ttu-id="fb432-117">Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="fb432-117">The sku name.</span></span>

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

### <span data-ttu-id="fb432-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fb432-118">-SkuTier</span></span>
<span data-ttu-id="fb432-119">SKUTier.</span><span class="sxs-lookup"><span data-stu-id="fb432-119">SkuTier.</span></span>

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

### <span data-ttu-id="fb432-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb432-120">CommonParameters</span></span>
<span data-ttu-id="fb432-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb432-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb432-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb432-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb432-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb432-123">INPUTS</span></span>

## <span data-ttu-id="fb432-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb432-124">OUTPUTS</span></span>

### <span data-ttu-id="fb432-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="fb432-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="fb432-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb432-126">NOTES</span></span>

<span data-ttu-id="fb432-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fb432-127">ALIASES</span></span>

## <span data-ttu-id="fb432-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb432-128">RELATED LINKS</span></span>

