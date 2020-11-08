---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066166"
---
# <span data-ttu-id="626ae-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="626ae-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="626ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="626ae-102">SYNOPSIS</span></span>
<span data-ttu-id="626ae-103">Отмена регистрации поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="626ae-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="626ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="626ae-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626ae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="626ae-105">DESCRIPTION</span></span>
<span data-ttu-id="626ae-106">Командлет **Unregister-AzResourceProvider** отменяет регистрацию поставщика ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="626ae-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="626ae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="626ae-107">EXAMPLES</span></span>

### <span data-ttu-id="626ae-108">Пример 1: Отмена регистрации поставщика ресурсов с помощью ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="626ae-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="626ae-109">Эта команда отменяет регистрацию поставщика ресурсов "Microsoft. support".</span><span class="sxs-lookup"><span data-stu-id="626ae-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="626ae-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="626ae-110">PARAMETERS</span></span>

### <span data-ttu-id="626ae-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="626ae-111">-ApiVersion</span></span>
<span data-ttu-id="626ae-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="626ae-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="626ae-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="626ae-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="626ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626ae-114">-DefaultProfile</span></span>
<span data-ttu-id="626ae-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="626ae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="626ae-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="626ae-116">-Pre</span></span>
<span data-ttu-id="626ae-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="626ae-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="626ae-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="626ae-118">-ProviderNamespace</span></span>
<span data-ttu-id="626ae-119">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="626ae-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="626ae-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="626ae-120">-Confirm</span></span>
<span data-ttu-id="626ae-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="626ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626ae-122">-WhatIf</span></span>
<span data-ttu-id="626ae-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="626ae-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="626ae-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="626ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626ae-125">CommonParameters</span></span>
<span data-ttu-id="626ae-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="626ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626ae-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="626ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626ae-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="626ae-128">INPUTS</span></span>

### <span data-ttu-id="626ae-129">System. String</span><span class="sxs-lookup"><span data-stu-id="626ae-129">System.String</span></span>

## <span data-ttu-id="626ae-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="626ae-130">OUTPUTS</span></span>

### <span data-ttu-id="626ae-131">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="626ae-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="626ae-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="626ae-132">NOTES</span></span>

## <span data-ttu-id="626ae-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="626ae-133">RELATED LINKS</span></span>

[<span data-ttu-id="626ae-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="626ae-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="626ae-135">Регистрация — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="626ae-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


