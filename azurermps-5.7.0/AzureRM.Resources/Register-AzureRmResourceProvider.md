---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 9e379df74f974e303faac300515e6bb7844e770b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733226"
---
# <span data-ttu-id="5f940-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f940-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="5f940-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f940-102">SYNOPSIS</span></span>
<span data-ttu-id="5f940-103">Регистрация поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f940-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f940-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f940-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f940-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f940-105">DESCRIPTION</span></span>
<span data-ttu-id="5f940-106">Командлет **Register-AzureRmResourceProvider** регистрирует поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5f940-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="5f940-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f940-107">EXAMPLES</span></span>

### <span data-ttu-id="5f940-108">Пример 1: регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="5f940-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="5f940-109">В этом случае регистрируется служба Microsoft. Network для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5f940-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="5f940-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f940-110">PARAMETERS</span></span>

### <span data-ttu-id="5f940-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5f940-111">-ApiVersion</span></span>
<span data-ttu-id="5f940-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f940-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="5f940-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f940-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f940-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f940-114">-DefaultProfile</span></span>
<span data-ttu-id="5f940-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5f940-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f940-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="5f940-116">-Pre</span></span>
<span data-ttu-id="5f940-117">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="5f940-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f940-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5f940-118">-ProviderNamespace</span></span>
<span data-ttu-id="5f940-119">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5f940-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="5f940-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f940-120">-Confirm</span></span>
<span data-ttu-id="5f940-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5f940-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f940-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f940-122">-WhatIf</span></span>
<span data-ttu-id="5f940-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5f940-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f940-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5f940-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f940-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f940-125">CommonParameters</span></span>
<span data-ttu-id="5f940-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f940-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f940-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f940-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f940-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f940-128">INPUTS</span></span>

### <span data-ttu-id="5f940-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="5f940-129">None</span></span>
<span data-ttu-id="5f940-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5f940-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f940-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f940-131">OUTPUTS</span></span>

### <span data-ttu-id="5f940-132">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f940-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="5f940-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f940-133">NOTES</span></span>

## <span data-ttu-id="5f940-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f940-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f940-135">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f940-135">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="5f940-136">Отмена регистрации — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="5f940-136">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


