---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/unregister-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Unregister-AzureRmResourceProvider.md
ms.openlocfilehash: d957859fc03a5d8beec90190d473240acb7b2482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734292"
---
# <span data-ttu-id="b9c38-101">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9c38-101">Unregister-AzureRmResourceProvider</span></span>

## <span data-ttu-id="b9c38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9c38-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c38-103">Отмена регистрации поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9c38-103">Unregisters a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9c38-104">SYNTAX</span></span>

```
Unregister-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9c38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9c38-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c38-106">Командлет **Unregister-AzureRmResourceProvider** отменяет регистрацию поставщика ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c38-106">The **Unregister-AzureRmResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="b9c38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9c38-107">EXAMPLES</span></span>

## <span data-ttu-id="b9c38-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9c38-108">PARAMETERS</span></span>

### <span data-ttu-id="b9c38-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b9c38-109">-ApiVersion</span></span>
<span data-ttu-id="b9c38-110">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9c38-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b9c38-111">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9c38-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b9c38-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c38-112">-DefaultProfile</span></span>
<span data-ttu-id="b9c38-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9c38-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9c38-114">-Pre</span><span class="sxs-lookup"><span data-stu-id="b9c38-114">-Pre</span></span>
<span data-ttu-id="b9c38-115">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="b9c38-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b9c38-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b9c38-116">-ProviderNamespace</span></span>
<span data-ttu-id="b9c38-117">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9c38-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="b9c38-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9c38-118">-Confirm</span></span>
<span data-ttu-id="b9c38-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9c38-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c38-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c38-120">-WhatIf</span></span>
<span data-ttu-id="b9c38-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9c38-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c38-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9c38-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c38-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c38-123">CommonParameters</span></span>
<span data-ttu-id="b9c38-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9c38-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c38-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c38-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c38-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9c38-126">INPUTS</span></span>

## <span data-ttu-id="b9c38-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9c38-127">OUTPUTS</span></span>

## <span data-ttu-id="b9c38-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9c38-128">NOTES</span></span>

## <span data-ttu-id="b9c38-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9c38-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9c38-130">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9c38-130">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="b9c38-131">Регистрация — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b9c38-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)


