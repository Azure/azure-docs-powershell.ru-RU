---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 11ff763dacc5a6969501dae925fbbc2382c871b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905558"
---
# <span data-ttu-id="a712a-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a712a-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="a712a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a712a-102">SYNOPSIS</span></span>
<span data-ttu-id="a712a-103">Регистрация поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a712a-103">Registers a resource provider.</span></span>

## <span data-ttu-id="a712a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a712a-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a712a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a712a-105">DESCRIPTION</span></span>
<span data-ttu-id="a712a-106">Командлет **Register-AzResourceProvider** регистрирует поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="a712a-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="a712a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a712a-107">EXAMPLES</span></span>

### <span data-ttu-id="a712a-108">Пример 1: регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="a712a-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="a712a-109">В этом случае регистрируется служба Microsoft. Network для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a712a-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="a712a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a712a-110">PARAMETERS</span></span>

### <span data-ttu-id="a712a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a712a-111">-ApiVersion</span></span>
<span data-ttu-id="a712a-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a712a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a712a-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a712a-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a712a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a712a-114">-DefaultProfile</span></span>
<span data-ttu-id="a712a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a712a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a712a-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="a712a-116">-Pre</span></span>
<span data-ttu-id="a712a-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a712a-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a712a-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a712a-118">-ProviderNamespace</span></span>
<span data-ttu-id="a712a-119">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a712a-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="a712a-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a712a-120">-Confirm</span></span>
<span data-ttu-id="a712a-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a712a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a712a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a712a-122">-WhatIf</span></span>
<span data-ttu-id="a712a-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a712a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a712a-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a712a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a712a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a712a-125">CommonParameters</span></span>
<span data-ttu-id="a712a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a712a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a712a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a712a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a712a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a712a-128">INPUTS</span></span>

### <span data-ttu-id="a712a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a712a-129">System.String</span></span>

## <span data-ttu-id="a712a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a712a-130">OUTPUTS</span></span>

### <span data-ttu-id="a712a-131">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a712a-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="a712a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a712a-132">NOTES</span></span>

## <span data-ttu-id="a712a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a712a-133">RELATED LINKS</span></span>

[<span data-ttu-id="a712a-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a712a-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="a712a-135">Отмена регистрации — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a712a-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


