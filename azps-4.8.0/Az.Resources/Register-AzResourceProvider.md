---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234778"
---
# <span data-ttu-id="f2744-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f2744-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="f2744-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2744-102">SYNOPSIS</span></span>
<span data-ttu-id="f2744-103">Регистрация поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2744-103">Registers a resource provider.</span></span>

## <span data-ttu-id="f2744-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2744-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2744-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2744-105">DESCRIPTION</span></span>
<span data-ttu-id="f2744-106">Командлет **Register-AzResourceProvider** регистрирует поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f2744-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="f2744-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2744-107">EXAMPLES</span></span>

### <span data-ttu-id="f2744-108">Пример 1: регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="f2744-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="f2744-109">В этом случае регистрируется служба Microsoft. Network для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f2744-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="f2744-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2744-110">PARAMETERS</span></span>

### <span data-ttu-id="f2744-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2744-111">-ApiVersion</span></span>
<span data-ttu-id="f2744-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2744-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f2744-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2744-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f2744-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2744-114">-DefaultProfile</span></span>
<span data-ttu-id="f2744-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f2744-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2744-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="f2744-116">-Pre</span></span>
<span data-ttu-id="f2744-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="f2744-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f2744-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f2744-118">-ProviderNamespace</span></span>
<span data-ttu-id="f2744-119">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2744-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="f2744-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2744-120">-Confirm</span></span>
<span data-ttu-id="f2744-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2744-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2744-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2744-122">-WhatIf</span></span>
<span data-ttu-id="f2744-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2744-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2744-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2744-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2744-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2744-125">CommonParameters</span></span>
<span data-ttu-id="f2744-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2744-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2744-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2744-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2744-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2744-128">INPUTS</span></span>

### <span data-ttu-id="f2744-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f2744-129">System.String</span></span>

## <span data-ttu-id="f2744-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2744-130">OUTPUTS</span></span>

### <span data-ttu-id="f2744-131">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f2744-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="f2744-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2744-132">NOTES</span></span>

## <span data-ttu-id="f2744-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2744-133">RELATED LINKS</span></span>

[<span data-ttu-id="f2744-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f2744-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="f2744-135">Отмена регистрации — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f2744-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


