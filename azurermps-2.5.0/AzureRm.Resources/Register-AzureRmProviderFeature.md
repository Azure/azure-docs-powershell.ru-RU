---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914706"
---
# <span data-ttu-id="306a2-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="306a2-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="306a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="306a2-102">SYNOPSIS</span></span>
<span data-ttu-id="306a2-103">Регистрация компонента поставщика Azure в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="306a2-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="306a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="306a2-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="306a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="306a2-105">DESCRIPTION</span></span>
<span data-ttu-id="306a2-106">Командлет **Register-AzureRmProviderFeature** регистрирует функцию поставщика Azure в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="306a2-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="306a2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="306a2-107">EXAMPLES</span></span>

### <span data-ttu-id="306a2-108">Пример 1: регистрация функции</span><span class="sxs-lookup"><span data-stu-id="306a2-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="306a2-109">Будет добавлена функция AllowApplicationSecurityGroups для Microsoft. Network для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="306a2-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="306a2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="306a2-110">PARAMETERS</span></span>

### <span data-ttu-id="306a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="306a2-111">-DefaultProfile</span></span>
<span data-ttu-id="306a2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="306a2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="306a2-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="306a2-113">-FeatureName</span></span>
<span data-ttu-id="306a2-114">Указывает имя компонента, который регистрируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="306a2-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="306a2-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="306a2-115">-ProviderNamespace</span></span>
<span data-ttu-id="306a2-116">Задает пространство имен, для которого этот командлет регистрирует функцию поставщика.</span><span class="sxs-lookup"><span data-stu-id="306a2-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="306a2-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="306a2-117">-Confirm</span></span>
<span data-ttu-id="306a2-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="306a2-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="306a2-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="306a2-119">-WhatIf</span></span>
<span data-ttu-id="306a2-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="306a2-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="306a2-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="306a2-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="306a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="306a2-122">CommonParameters</span></span>
<span data-ttu-id="306a2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="306a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="306a2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="306a2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="306a2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="306a2-125">INPUTS</span></span>

## <span data-ttu-id="306a2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="306a2-126">OUTPUTS</span></span>

## <span data-ttu-id="306a2-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="306a2-127">NOTES</span></span>

## <span data-ttu-id="306a2-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="306a2-128">RELATED LINKS</span></span>

[<span data-ttu-id="306a2-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="306a2-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


