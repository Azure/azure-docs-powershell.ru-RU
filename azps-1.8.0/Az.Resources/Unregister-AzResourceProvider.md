---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: de2a213122f756d87255be6195759e467f64b428
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729294"
---
# <span data-ttu-id="a1a3b-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a1a3b-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="a1a3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a3b-103">Отмена регистрации поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="a1a3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1a3b-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1a3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1a3b-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a3b-106">Командлет **Unregister-AzResourceProvider** отменяет регистрацию поставщика ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="a1a3b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1a3b-107">EXAMPLES</span></span>

## <span data-ttu-id="a1a3b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1a3b-108">PARAMETERS</span></span>

### <span data-ttu-id="a1a3b-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a1a3b-109">-ApiVersion</span></span>
<span data-ttu-id="a1a3b-110">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a1a3b-111">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a1a3b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a3b-112">-DefaultProfile</span></span>
<span data-ttu-id="a1a3b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a1a3b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1a3b-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="a1a3b-114">-Pre</span></span>
<span data-ttu-id="a1a3b-115">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1a3b-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a1a3b-116">-ProviderNamespace</span></span>
<span data-ttu-id="a1a3b-117">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="a1a3b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1a3b-118">-Confirm</span></span>
<span data-ttu-id="a1a3b-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a3b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a3b-120">-WhatIf</span></span>
<span data-ttu-id="a1a3b-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1a3b-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a3b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a3b-123">CommonParameters</span></span>
<span data-ttu-id="a1a3b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1a3b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a3b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1a3b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a3b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1a3b-126">INPUTS</span></span>

### <span data-ttu-id="a1a3b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a1a3b-127">System.String</span></span>

## <span data-ttu-id="a1a3b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1a3b-128">OUTPUTS</span></span>

### <span data-ttu-id="a1a3b-129">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a1a3b-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="a1a3b-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1a3b-130">NOTES</span></span>

## <span data-ttu-id="a1a3b-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1a3b-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1a3b-132">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a1a3b-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="a1a3b-133">Регистрация — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a1a3b-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


