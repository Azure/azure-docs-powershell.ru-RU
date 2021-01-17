---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406940"
---
# <span data-ttu-id="af6d0-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="af6d0-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="af6d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="af6d0-103">Регистрация функции поставщика Azure в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="af6d0-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="af6d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af6d0-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af6d0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af6d0-105">DESCRIPTION</span></span>
<span data-ttu-id="af6d0-106">**Cmdlet Register-AzProviderFeature** регистрирует функцию поставщика Azure в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="af6d0-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="af6d0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af6d0-107">EXAMPLES</span></span>

### <span data-ttu-id="af6d0-108">Пример 1. Регистрация функции</span><span class="sxs-lookup"><span data-stu-id="af6d0-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="af6d0-109">При этом в вашу учетную запись будет добавлена функция AllowApplicationSecurityGroups для Microsoft.Network.</span><span class="sxs-lookup"><span data-stu-id="af6d0-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="af6d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af6d0-110">PARAMETERS</span></span>

### <span data-ttu-id="af6d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af6d0-111">-DefaultProfile</span></span>
<span data-ttu-id="af6d0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af6d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6d0-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="af6d0-113">-FeatureName</span></span>
<span data-ttu-id="af6d0-114">Указывает имя функции, регистрируется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af6d0-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af6d0-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="af6d0-115">-ProviderNamespace</span></span>
<span data-ttu-id="af6d0-116">Определяет пространство имен, для которого этот cmdlet регистрирует функцию поставщика.</span><span class="sxs-lookup"><span data-stu-id="af6d0-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af6d0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af6d0-117">-Confirm</span></span>
<span data-ttu-id="af6d0-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="af6d0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6d0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af6d0-119">-WhatIf</span></span>
<span data-ttu-id="af6d0-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af6d0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af6d0-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af6d0-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af6d0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af6d0-122">CommonParameters</span></span>
<span data-ttu-id="af6d0-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af6d0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af6d0-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af6d0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af6d0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af6d0-125">INPUTS</span></span>

### <span data-ttu-id="af6d0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="af6d0-126">System.String</span></span>

## <span data-ttu-id="af6d0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af6d0-127">OUTPUTS</span></span>

### <span data-ttu-id="af6d0-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="af6d0-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="af6d0-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af6d0-129">NOTES</span></span>

## <span data-ttu-id="af6d0-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af6d0-130">RELATED LINKS</span></span>

[<span data-ttu-id="af6d0-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="af6d0-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


