---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 67a0eee0dfe46b7b846958e1aa3f2be515a6b213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016051"
---
# <span data-ttu-id="fe5aa-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fe5aa-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="fe5aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5aa-103">Сведения о службах поставщиков Azure.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="fe5aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe5aa-104">SYNTAX</span></span>

### <span data-ttu-id="fe5aa-105">ListAvailableParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe5aa-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe5aa-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="fe5aa-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe5aa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe5aa-107">DESCRIPTION</span></span>
<span data-ttu-id="fe5aa-108">Для функций поставщика Azure можно получить имя, имя поставщика и состояние регистрации для **get-AzProviderFeature.**</span><span class="sxs-lookup"><span data-stu-id="fe5aa-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="fe5aa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe5aa-109">EXAMPLES</span></span>

### <span data-ttu-id="fe5aa-110">Пример 1. Доступ к всем доступным функциям</span><span class="sxs-lookup"><span data-stu-id="fe5aa-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="fe5aa-111">Эта команда получает все доступные функции.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-111">This command gets all available features.</span></span>

### <span data-ttu-id="fe5aa-112">Пример 2. Просмотр сведений об определенной функции</span><span class="sxs-lookup"><span data-stu-id="fe5aa-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="fe5aa-113">Эта команда получает сведения о функции AllowPreReleaseRegions для указанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="fe5aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe5aa-114">PARAMETERS</span></span>

### <span data-ttu-id="fe5aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5aa-115">-DefaultProfile</span></span>
<span data-ttu-id="fe5aa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe5aa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe5aa-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="fe5aa-117">-FeatureName</span></span>
<span data-ttu-id="fe5aa-118">Указывает имя функции, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5aa-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="fe5aa-119">-ListAvailable</span></span>
<span data-ttu-id="fe5aa-120">Указывает на то, что этот cmdlet получает все функции.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5aa-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fe5aa-121">-ProviderNamespace</span></span>
<span data-ttu-id="fe5aa-122">Определяет пространство имен, для которого этот cmdlet получает функции поставщика.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe5aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5aa-123">CommonParameters</span></span>
<span data-ttu-id="fe5aa-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe5aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5aa-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe5aa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5aa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe5aa-126">INPUTS</span></span>

### <span data-ttu-id="fe5aa-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fe5aa-127">System.String</span></span>

## <span data-ttu-id="fe5aa-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe5aa-128">OUTPUTS</span></span>

### <span data-ttu-id="fe5aa-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fe5aa-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="fe5aa-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe5aa-130">NOTES</span></span>

## <span data-ttu-id="fe5aa-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe5aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe5aa-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fe5aa-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


