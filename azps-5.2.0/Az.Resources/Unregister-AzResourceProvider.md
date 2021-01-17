---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401148"
---
# <span data-ttu-id="7090f-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7090f-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="7090f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7090f-102">SYNOPSIS</span></span>
<span data-ttu-id="7090f-103">Отрегистрет поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7090f-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="7090f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7090f-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7090f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7090f-105">DESCRIPTION</span></span>
<span data-ttu-id="7090f-106">**Из-за cmdister-AzResourceProvider** поставщик ресурсов Azure будет отсутствован.</span><span class="sxs-lookup"><span data-stu-id="7090f-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="7090f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7090f-107">EXAMPLES</span></span>

### <span data-ttu-id="7090f-108">Пример 1. Unregister resource provider with ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7090f-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="7090f-109">Эта команда отвязкает поставщика ресурсов "Microsoft.support".</span><span class="sxs-lookup"><span data-stu-id="7090f-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="7090f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7090f-110">PARAMETERS</span></span>

### <span data-ttu-id="7090f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7090f-111">-ApiVersion</span></span>
<span data-ttu-id="7090f-112">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7090f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7090f-113">Можно указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7090f-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7090f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7090f-114">-DefaultProfile</span></span>
<span data-ttu-id="7090f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7090f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7090f-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="7090f-116">-Pre</span></span>
<span data-ttu-id="7090f-117">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="7090f-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7090f-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7090f-118">-ProviderNamespace</span></span>
<span data-ttu-id="7090f-119">Определяет пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7090f-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="7090f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7090f-120">-Confirm</span></span>
<span data-ttu-id="7090f-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7090f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7090f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7090f-122">-WhatIf</span></span>
<span data-ttu-id="7090f-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7090f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7090f-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7090f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7090f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7090f-125">CommonParameters</span></span>
<span data-ttu-id="7090f-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7090f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7090f-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7090f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7090f-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7090f-128">INPUTS</span></span>

### <span data-ttu-id="7090f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7090f-129">System.String</span></span>

## <span data-ttu-id="7090f-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7090f-130">OUTPUTS</span></span>

### <span data-ttu-id="7090f-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7090f-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="7090f-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7090f-132">NOTES</span></span>

## <span data-ttu-id="7090f-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7090f-133">RELATED LINKS</span></span>

[<span data-ttu-id="7090f-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7090f-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="7090f-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7090f-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


