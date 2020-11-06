---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567070"
---
# <span data-ttu-id="e9747-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e9747-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="e9747-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9747-102">SYNOPSIS</span></span>
<span data-ttu-id="e9747-103">Регистрация компонента поставщика Azure в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e9747-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9747-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9747-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9747-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9747-105">DESCRIPTION</span></span>
<span data-ttu-id="e9747-106">Командлет **Register-AzureRmProviderFeature** регистрирует функцию поставщика Azure в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e9747-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="e9747-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9747-107">EXAMPLES</span></span>

## <span data-ttu-id="e9747-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9747-108">PARAMETERS</span></span>

### <span data-ttu-id="e9747-109">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="e9747-109">-FeatureName</span></span>
<span data-ttu-id="e9747-110">Указывает имя компонента, который регистрируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e9747-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="e9747-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e9747-111">-ProviderNamespace</span></span>
<span data-ttu-id="e9747-112">Задает пространство имен, для которого этот командлет регистрирует функцию поставщика.</span><span class="sxs-lookup"><span data-stu-id="e9747-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="e9747-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9747-113">-Confirm</span></span>
<span data-ttu-id="e9747-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9747-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9747-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9747-115">-WhatIf</span></span>
<span data-ttu-id="e9747-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9747-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9747-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9747-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9747-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9747-118">-DefaultProfile</span></span>
<span data-ttu-id="e9747-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9747-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9747-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9747-120">CommonParameters</span></span>
<span data-ttu-id="e9747-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9747-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9747-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9747-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9747-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9747-123">INPUTS</span></span>

## <span data-ttu-id="e9747-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9747-124">OUTPUTS</span></span>

### <span data-ttu-id="e9747-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="e9747-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="e9747-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9747-126">NOTES</span></span>

## <span data-ttu-id="e9747-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9747-127">RELATED LINKS</span></span>

[<span data-ttu-id="e9747-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e9747-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


