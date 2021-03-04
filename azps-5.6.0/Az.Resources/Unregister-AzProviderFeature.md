---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 30c315240cf667db37c6c605cda093fe7811a3ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959464"
---
# <span data-ttu-id="24755-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="24755-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="24755-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24755-102">SYNOPSIS</span></span>
<span data-ttu-id="24755-103">В вашей учетной записи будет отрегистрирован поставщик Azure.</span><span class="sxs-lookup"><span data-stu-id="24755-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="24755-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24755-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24755-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24755-105">DESCRIPTION</span></span>
<span data-ttu-id="24755-106">Для регистрации поставщика Azure в вашей учетной записи будет **cmdlet Unregister-AzProviderFeature.**</span><span class="sxs-lookup"><span data-stu-id="24755-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="24755-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24755-107">EXAMPLES</span></span>

### <span data-ttu-id="24755-108">Пример 1. Отрегистрации функции</span><span class="sxs-lookup"><span data-stu-id="24755-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="24755-109">В этом случае функция AllowApplicationSecurityGroups для Microsoft.Network будет отрегистрирована в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="24755-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="24755-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24755-110">PARAMETERS</span></span>

### <span data-ttu-id="24755-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24755-111">-DefaultProfile</span></span>
<span data-ttu-id="24755-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24755-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24755-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="24755-113">-FeatureName</span></span>
<span data-ttu-id="24755-114">Название функции.</span><span class="sxs-lookup"><span data-stu-id="24755-114">The feature name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24755-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="24755-115">-ProviderNamespace</span></span>
<span data-ttu-id="24755-116">Пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24755-116">The resource provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24755-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24755-117">-Confirm</span></span>
<span data-ttu-id="24755-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24755-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24755-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24755-119">-WhatIf</span></span>
<span data-ttu-id="24755-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24755-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24755-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="24755-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24755-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24755-122">CommonParameters</span></span>
<span data-ttu-id="24755-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24755-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24755-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24755-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24755-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24755-125">INPUTS</span></span>

### <span data-ttu-id="24755-126">System.String</span><span class="sxs-lookup"><span data-stu-id="24755-126">System.String</span></span>

## <span data-ttu-id="24755-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24755-127">OUTPUTS</span></span>

### <span data-ttu-id="24755-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="24755-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="24755-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24755-129">NOTES</span></span>

## <span data-ttu-id="24755-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24755-130">RELATED LINKS</span></span>