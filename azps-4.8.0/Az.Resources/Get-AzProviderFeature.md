---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242686"
---
# <span data-ttu-id="112af-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="112af-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="112af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="112af-102">SYNOPSIS</span></span>
<span data-ttu-id="112af-103">Получение сведений о возможностях поставщика Azure.</span><span class="sxs-lookup"><span data-stu-id="112af-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="112af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="112af-104">SYNTAX</span></span>

### <span data-ttu-id="112af-105">ListAvailableParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="112af-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="112af-106">Функция функцию</span><span class="sxs-lookup"><span data-stu-id="112af-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="112af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="112af-107">DESCRIPTION</span></span>
<span data-ttu-id="112af-108">Командлет **Get-AzProviderFeature** получает имя компонента, имя поставщика и состояние регистрации для функций поставщика Azure.</span><span class="sxs-lookup"><span data-stu-id="112af-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="112af-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="112af-109">EXAMPLES</span></span>

### <span data-ttu-id="112af-110">Пример 1: получение всех доступных функций</span><span class="sxs-lookup"><span data-stu-id="112af-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="112af-111">Эта команда получает все доступные функции.</span><span class="sxs-lookup"><span data-stu-id="112af-111">This command gets all available features.</span></span>

### <span data-ttu-id="112af-112">Пример 2: получение сведений о конкретном компоненте</span><span class="sxs-lookup"><span data-stu-id="112af-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="112af-113">Эта команда получает сведения о компоненте с именем AllowPreReleaseRegions для указанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="112af-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="112af-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="112af-114">PARAMETERS</span></span>

### <span data-ttu-id="112af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112af-115">-DefaultProfile</span></span>
<span data-ttu-id="112af-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="112af-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="112af-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="112af-117">-FeatureName</span></span>
<span data-ttu-id="112af-118">Указывает имя компонента, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="112af-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="112af-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="112af-119">-ListAvailable</span></span>
<span data-ttu-id="112af-120">Указывает на то, что этот командлет получает все компоненты.</span><span class="sxs-lookup"><span data-stu-id="112af-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="112af-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="112af-121">-ProviderNamespace</span></span>
<span data-ttu-id="112af-122">Задает пространство имен, для которого этот командлет получает функции поставщика.</span><span class="sxs-lookup"><span data-stu-id="112af-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="112af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112af-123">CommonParameters</span></span>
<span data-ttu-id="112af-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="112af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112af-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="112af-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112af-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="112af-126">INPUTS</span></span>

### <span data-ttu-id="112af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="112af-127">System.String</span></span>

## <span data-ttu-id="112af-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="112af-128">OUTPUTS</span></span>

### <span data-ttu-id="112af-129">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="112af-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="112af-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="112af-130">NOTES</span></span>

## <span data-ttu-id="112af-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="112af-131">RELATED LINKS</span></span>

[<span data-ttu-id="112af-132">Регистрация — AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="112af-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)

