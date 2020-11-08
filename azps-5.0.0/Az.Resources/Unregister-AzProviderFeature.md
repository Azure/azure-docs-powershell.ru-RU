---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248201"
---
# <span data-ttu-id="f1574-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f1574-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="f1574-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1574-102">SYNOPSIS</span></span>
<span data-ttu-id="f1574-103">Отмена регистрации функции поставщика Azure в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1574-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="f1574-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1574-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1574-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1574-105">DESCRIPTION</span></span>
<span data-ttu-id="f1574-106">Командлет **Unregister-AzProviderFeature** отменяет регистрацию компонента Azure provider в учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1574-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="f1574-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1574-107">EXAMPLES</span></span>

### <span data-ttu-id="f1574-108">Пример 1: Отмена регистрации функции</span><span class="sxs-lookup"><span data-stu-id="f1574-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="f1574-109">После этого функция AllowApplicationSecurityGroups для Microsoft. Network будет отменена из своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1574-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="f1574-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1574-110">PARAMETERS</span></span>

### <span data-ttu-id="f1574-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1574-111">-DefaultProfile</span></span>
<span data-ttu-id="f1574-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1574-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1574-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="f1574-113">-FeatureName</span></span>
<span data-ttu-id="f1574-114">Имя компонента.</span><span class="sxs-lookup"><span data-stu-id="f1574-114">The feature name.</span></span>

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

### <span data-ttu-id="f1574-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f1574-115">-ProviderNamespace</span></span>
<span data-ttu-id="f1574-116">Пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1574-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="f1574-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1574-117">-Confirm</span></span>
<span data-ttu-id="f1574-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1574-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1574-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1574-119">-WhatIf</span></span>
<span data-ttu-id="f1574-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1574-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1574-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1574-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1574-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1574-122">CommonParameters</span></span>
<span data-ttu-id="f1574-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1574-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1574-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1574-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1574-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1574-125">INPUTS</span></span>

### <span data-ttu-id="f1574-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f1574-126">System.String</span></span>

## <span data-ttu-id="f1574-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1574-127">OUTPUTS</span></span>

### <span data-ttu-id="f1574-128">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f1574-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="f1574-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1574-129">NOTES</span></span>

## <span data-ttu-id="f1574-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1574-130">RELATED LINKS</span></span>