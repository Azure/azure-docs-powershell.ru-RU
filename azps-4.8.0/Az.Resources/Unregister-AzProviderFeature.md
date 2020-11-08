---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 6cb27f66871038fa1849671391e1d7d9f8f3ccd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235385"
---
# <span data-ttu-id="9a053-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="9a053-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="9a053-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a053-102">SYNOPSIS</span></span>
<span data-ttu-id="9a053-103">Отмена регистрации функции поставщика Azure в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a053-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="9a053-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a053-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a053-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a053-105">DESCRIPTION</span></span>
<span data-ttu-id="9a053-106">Командлет **Unregister-AzProviderFeature** отменяет регистрацию компонента Azure provider в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a053-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="9a053-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a053-107">EXAMPLES</span></span>

### <span data-ttu-id="9a053-108">Пример 1: Отмена регистрации функции</span><span class="sxs-lookup"><span data-stu-id="9a053-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="9a053-109">После этого функция AllowApplicationSecurityGroups для Microsoft. Network будет отменена из своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9a053-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="9a053-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a053-110">PARAMETERS</span></span>

### <span data-ttu-id="9a053-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a053-111">-DefaultProfile</span></span>
<span data-ttu-id="9a053-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a053-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a053-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="9a053-113">-FeatureName</span></span>
<span data-ttu-id="9a053-114">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="9a053-114">The feature name.</span></span>

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

### <span data-ttu-id="9a053-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="9a053-115">-ProviderNamespace</span></span>
<span data-ttu-id="9a053-116">Пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a053-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="9a053-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a053-117">-Confirm</span></span>
<span data-ttu-id="9a053-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a053-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a053-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a053-119">-WhatIf</span></span>
<span data-ttu-id="9a053-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a053-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a053-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a053-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a053-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a053-122">CommonParameters</span></span>
<span data-ttu-id="9a053-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a053-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a053-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a053-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a053-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a053-125">INPUTS</span></span>

### <span data-ttu-id="9a053-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9a053-126">System.String</span></span>

## <span data-ttu-id="9a053-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a053-127">OUTPUTS</span></span>

### <span data-ttu-id="9a053-128">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="9a053-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="9a053-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a053-129">NOTES</span></span>

## <span data-ttu-id="9a053-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a053-130">RELATED LINKS</span></span>
