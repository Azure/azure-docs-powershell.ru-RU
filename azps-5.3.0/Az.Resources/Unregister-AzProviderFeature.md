---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507642"
---
# <span data-ttu-id="2a0c6-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="2a0c6-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="2a0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0c6-103">В вашей учетной записи будет отрегистрирован поставщик Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="2a0c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a0c6-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a0c6-105">DESCRIPTION</span></span>
<span data-ttu-id="2a0c6-106">Для регистрации поставщика Azure в вашей учетной записи будет **cmdlet Unregister-AzProviderFeature.**</span><span class="sxs-lookup"><span data-stu-id="2a0c6-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="2a0c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a0c6-107">EXAMPLES</span></span>

### <span data-ttu-id="2a0c6-108">Пример 1. Отрегистрации функции</span><span class="sxs-lookup"><span data-stu-id="2a0c6-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="2a0c6-109">В этом случае функция AllowApplicationSecurityGroups для Microsoft.Network будет отрегистрирована в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="2a0c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a0c6-110">PARAMETERS</span></span>

### <span data-ttu-id="2a0c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0c6-111">-DefaultProfile</span></span>
<span data-ttu-id="2a0c6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a0c6-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="2a0c6-113">-FeatureName</span></span>
<span data-ttu-id="2a0c6-114">Название функции.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-114">The feature name.</span></span>

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

### <span data-ttu-id="2a0c6-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="2a0c6-115">-ProviderNamespace</span></span>
<span data-ttu-id="2a0c6-116">Пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="2a0c6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a0c6-117">-Confirm</span></span>
<span data-ttu-id="2a0c6-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0c6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0c6-119">-WhatIf</span></span>
<span data-ttu-id="2a0c6-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0c6-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0c6-122">CommonParameters</span></span>
<span data-ttu-id="2a0c6-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0c6-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a0c6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0c6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a0c6-125">INPUTS</span></span>

### <span data-ttu-id="2a0c6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2a0c6-126">System.String</span></span>

## <span data-ttu-id="2a0c6-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a0c6-127">OUTPUTS</span></span>

### <span data-ttu-id="2a0c6-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="2a0c6-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="2a0c6-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a0c6-129">NOTES</span></span>

## <span data-ttu-id="2a0c6-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a0c6-130">RELATED LINKS</span></span>