---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: c3459a07eb6f92e4ec30b5018efc41ff13e1c41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914698"
---
# <span data-ttu-id="aa245-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="aa245-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="aa245-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa245-102">SYNOPSIS</span></span>
<span data-ttu-id="aa245-103">Регистрация поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa245-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa245-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa245-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa245-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa245-105">DESCRIPTION</span></span>
<span data-ttu-id="aa245-106">Командлет **Register-AzureRmResourceProvider** регистрирует поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="aa245-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="aa245-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa245-107">EXAMPLES</span></span>

### <span data-ttu-id="aa245-108">Пример 1: регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="aa245-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="aa245-109">В этом случае регистрируется служба Microsoft. Network для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aa245-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="aa245-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa245-110">PARAMETERS</span></span>

### <span data-ttu-id="aa245-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aa245-111">-ApiVersion</span></span>
<span data-ttu-id="aa245-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa245-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="aa245-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa245-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="aa245-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa245-114">-DefaultProfile</span></span>
<span data-ttu-id="aa245-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa245-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa245-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="aa245-116">-Pre</span></span>
<span data-ttu-id="aa245-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="aa245-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aa245-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="aa245-118">-ProviderNamespace</span></span>
<span data-ttu-id="aa245-119">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa245-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="aa245-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa245-120">-Confirm</span></span>
<span data-ttu-id="aa245-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa245-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa245-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa245-122">-WhatIf</span></span>
<span data-ttu-id="aa245-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa245-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa245-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa245-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa245-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa245-125">CommonParameters</span></span>
<span data-ttu-id="aa245-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa245-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa245-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa245-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa245-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa245-128">INPUTS</span></span>

## <span data-ttu-id="aa245-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa245-129">OUTPUTS</span></span>

## <span data-ttu-id="aa245-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa245-130">NOTES</span></span>

## <span data-ttu-id="aa245-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa245-131">RELATED LINKS</span></span>

[<span data-ttu-id="aa245-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="aa245-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="aa245-133">Отмена регистрации — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="aa245-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


