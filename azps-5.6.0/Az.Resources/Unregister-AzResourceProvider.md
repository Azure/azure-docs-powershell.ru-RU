---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: c51cb2eaa00e870eee3e70e0e86c4da3fb36a330
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959432"
---
# <span data-ttu-id="e9cf1-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9cf1-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="e9cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="e9cf1-103">Отрегистрет поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="e9cf1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e9cf1-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9cf1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9cf1-105">DESCRIPTION</span></span>
<span data-ttu-id="e9cf1-106">**Из-за cmdister-AzResourceProvider** поставщик ресурсов Azure будет отсутствован.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="e9cf1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e9cf1-107">EXAMPLES</span></span>

### <span data-ttu-id="e9cf1-108">Пример 1. Unregister resource provider with ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e9cf1-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="e9cf1-109">Эта команда отвязкает поставщика ресурсов "Microsoft.support".</span><span class="sxs-lookup"><span data-stu-id="e9cf1-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="e9cf1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9cf1-110">PARAMETERS</span></span>

### <span data-ttu-id="e9cf1-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e9cf1-111">-ApiVersion</span></span>
<span data-ttu-id="e9cf1-112">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e9cf1-113">Можно указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e9cf1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9cf1-114">-DefaultProfile</span></span>
<span data-ttu-id="e9cf1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e9cf1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9cf1-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="e9cf1-116">-Pre</span></span>
<span data-ttu-id="e9cf1-117">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9cf1-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e9cf1-118">-ProviderNamespace</span></span>
<span data-ttu-id="e9cf1-119">Определяет пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e9cf1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9cf1-120">-Confirm</span></span>
<span data-ttu-id="e9cf1-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9cf1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9cf1-122">-WhatIf</span></span>
<span data-ttu-id="e9cf1-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9cf1-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9cf1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9cf1-125">CommonParameters</span></span>
<span data-ttu-id="e9cf1-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9cf1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9cf1-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9cf1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9cf1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9cf1-128">INPUTS</span></span>

### <span data-ttu-id="e9cf1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e9cf1-129">System.String</span></span>

## <span data-ttu-id="e9cf1-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e9cf1-130">OUTPUTS</span></span>

### <span data-ttu-id="e9cf1-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9cf1-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="e9cf1-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e9cf1-132">NOTES</span></span>

## <span data-ttu-id="e9cf1-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9cf1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9cf1-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9cf1-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e9cf1-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e9cf1-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


