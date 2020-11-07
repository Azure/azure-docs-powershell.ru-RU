---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: c179ac3657a69b908c605fbaf4d0577b8a77a90f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910806"
---
# <span data-ttu-id="f644f-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f644f-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="f644f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f644f-102">SYNOPSIS</span></span>
<span data-ttu-id="f644f-103">Отмена регистрации поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f644f-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="f644f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f644f-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f644f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f644f-105">DESCRIPTION</span></span>
<span data-ttu-id="f644f-106">Командлет **Unregister-AzResourceProvider** отменяет регистрацию поставщика ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f644f-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="f644f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f644f-107">EXAMPLES</span></span>

## <span data-ttu-id="f644f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f644f-108">PARAMETERS</span></span>

### <span data-ttu-id="f644f-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f644f-109">-ApiVersion</span></span>
<span data-ttu-id="f644f-110">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f644f-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f644f-111">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f644f-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f644f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f644f-112">-DefaultProfile</span></span>
<span data-ttu-id="f644f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f644f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f644f-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="f644f-114">-Pre</span></span>
<span data-ttu-id="f644f-115">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f644f-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f644f-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f644f-116">-ProviderNamespace</span></span>
<span data-ttu-id="f644f-117">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f644f-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="f644f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f644f-118">-Confirm</span></span>
<span data-ttu-id="f644f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f644f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f644f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f644f-120">-WhatIf</span></span>
<span data-ttu-id="f644f-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f644f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f644f-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f644f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f644f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f644f-123">CommonParameters</span></span>
<span data-ttu-id="f644f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f644f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f644f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f644f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f644f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f644f-126">INPUTS</span></span>

## <span data-ttu-id="f644f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f644f-127">OUTPUTS</span></span>

## <span data-ttu-id="f644f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f644f-128">NOTES</span></span>

## <span data-ttu-id="f644f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f644f-129">RELATED LINKS</span></span>

[<span data-ttu-id="f644f-130">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f644f-130">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="f644f-131">Регистрация — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f644f-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


