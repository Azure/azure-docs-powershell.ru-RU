---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010051"
---
# <span data-ttu-id="32744-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="32744-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="32744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32744-102">SYNOPSIS</span></span>
<span data-ttu-id="32744-103">Удаляет существующий регион развертывания из экземпляра PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="32744-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="32744-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="32744-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32744-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32744-105">DESCRIPTION</span></span>
<span data-ttu-id="32744-106">Командлет **Remove-AzApiManagementRegion** удаляет экземпляр типа **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** из коллекции **AdditionalRegions** предоставленного экземпляра **типа Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="32744-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="32744-107">Этот cmdlet не изменяют само развертывание, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="32744-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="32744-108">Чтобы обновить развертывание управления API, передать измененный **psApiManagementInstance** в **Set-AzApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="32744-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="32744-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="32744-109">EXAMPLES</span></span>

### <span data-ttu-id="32744-110">Пример 1. Удаление области из экземпляра PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="32744-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="32744-111">Эта команда удаляет регион "Восток. США" из экземпляра **PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="32744-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="32744-112">Пример 2. Удаление области из экземпляра PsApiManagement с помощью ряда команд</span><span class="sxs-lookup"><span data-stu-id="32744-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="32744-113">Эта первая команда получает экземпляр **PsApiManagement** из группы ресурсов Contoso с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="32744-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="32744-114">Затем конечная команда удаляет регион "Восток. США" из этого экземпляра, а затем обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="32744-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="32744-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32744-115">PARAMETERS</span></span>

### <span data-ttu-id="32744-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="32744-116">-ApiManagement</span></span>
<span data-ttu-id="32744-117">Указывает экземпляр **PsApiManagement,** из который этот cmdlet удаляет дополнительный регион развертывания.</span><span class="sxs-lookup"><span data-stu-id="32744-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32744-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32744-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="32744-119">-Location</span><span class="sxs-lookup"><span data-stu-id="32744-119">-Location</span></span>
<span data-ttu-id="32744-120">Определяет расположение региона, который этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="32744-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="32744-121">Указывает расположение нового региона развертывания из поддерживаемого региона для службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="32744-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="32744-122">Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения</span><span class="sxs-lookup"><span data-stu-id="32744-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="32744-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32744-123">CommonParameters</span></span>
<span data-ttu-id="32744-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32744-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32744-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32744-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32744-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32744-126">INPUTS</span></span>

### <span data-ttu-id="32744-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="32744-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="32744-128">System.String</span><span class="sxs-lookup"><span data-stu-id="32744-128">System.String</span></span>

## <span data-ttu-id="32744-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="32744-129">OUTPUTS</span></span>

### <span data-ttu-id="32744-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="32744-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="32744-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="32744-131">NOTES</span></span>

## <span data-ttu-id="32744-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32744-132">RELATED LINKS</span></span>

[<span data-ttu-id="32744-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="32744-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="32744-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="32744-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


