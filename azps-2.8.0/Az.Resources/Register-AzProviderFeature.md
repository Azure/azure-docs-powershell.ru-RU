---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 57a01f831ab92b7ae8ca45fbf9535ed4fa7df0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904013"
---
# <span data-ttu-id="df706-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="df706-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="df706-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df706-102">SYNOPSIS</span></span>
<span data-ttu-id="df706-103">Регистрация компонента поставщика Azure в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="df706-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="df706-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df706-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df706-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df706-105">DESCRIPTION</span></span>
<span data-ttu-id="df706-106">Командлет **Register-AzProviderFeature** регистрирует функцию поставщика Azure в вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="df706-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="df706-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df706-107">EXAMPLES</span></span>

### <span data-ttu-id="df706-108">Пример 1: регистрация функции</span><span class="sxs-lookup"><span data-stu-id="df706-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="df706-109">Будет добавлена функция AllowApplicationSecurityGroups для Microsoft. Network для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="df706-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="df706-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df706-110">PARAMETERS</span></span>

### <span data-ttu-id="df706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df706-111">-DefaultProfile</span></span>
<span data-ttu-id="df706-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="df706-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df706-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="df706-113">-FeatureName</span></span>
<span data-ttu-id="df706-114">Указывает имя компонента, который регистрируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="df706-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="df706-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="df706-115">-ProviderNamespace</span></span>
<span data-ttu-id="df706-116">Задает пространство имен, для которого этот командлет регистрирует функцию поставщика.</span><span class="sxs-lookup"><span data-stu-id="df706-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="df706-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df706-117">-Confirm</span></span>
<span data-ttu-id="df706-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df706-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df706-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df706-119">-WhatIf</span></span>
<span data-ttu-id="df706-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df706-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df706-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df706-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df706-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df706-122">CommonParameters</span></span>
<span data-ttu-id="df706-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df706-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df706-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df706-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df706-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df706-125">INPUTS</span></span>

### <span data-ttu-id="df706-126">System. String</span><span class="sxs-lookup"><span data-stu-id="df706-126">System.String</span></span>

## <span data-ttu-id="df706-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df706-127">OUTPUTS</span></span>

### <span data-ttu-id="df706-128">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="df706-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="df706-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="df706-129">NOTES</span></span>

## <span data-ttu-id="df706-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df706-130">RELATED LINKS</span></span>

[<span data-ttu-id="df706-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="df706-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


