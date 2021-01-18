---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516602"
---
# <span data-ttu-id="b470b-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b470b-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="b470b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b470b-102">SYNOPSIS</span></span>
<span data-ttu-id="b470b-103">Возвращает все или определенные группы управления API.</span><span class="sxs-lookup"><span data-stu-id="b470b-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="b470b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b470b-104">SYNTAX</span></span>

### <span data-ttu-id="b470b-105">GetAllGroups (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b470b-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b470b-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="b470b-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b470b-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="b470b-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b470b-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="b470b-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b470b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b470b-109">DESCRIPTION</span></span>
<span data-ttu-id="b470b-110">Для **получения всех или определенных** групп управления API возвращается все или конкретные группы управления API.</span><span class="sxs-lookup"><span data-stu-id="b470b-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="b470b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b470b-111">EXAMPLES</span></span>

### <span data-ttu-id="b470b-112">Пример 1. Получить все группы</span><span class="sxs-lookup"><span data-stu-id="b470b-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="b470b-113">Эта команда возвращает все группы.</span><span class="sxs-lookup"><span data-stu-id="b470b-113">This command gets all groups.</span></span>

### <span data-ttu-id="b470b-114">Пример 2. Группировка по ИД</span><span class="sxs-lookup"><span data-stu-id="b470b-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="b470b-115">Эта команда получает групповой ИД 0123456789.</span><span class="sxs-lookup"><span data-stu-id="b470b-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="b470b-116">Пример 3. Получить группу по имени</span><span class="sxs-lookup"><span data-stu-id="b470b-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="b470b-117">Эта команда получает группу с именем Group0002.</span><span class="sxs-lookup"><span data-stu-id="b470b-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="b470b-118">Пример 4. Получить все группы пользователей</span><span class="sxs-lookup"><span data-stu-id="b470b-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="b470b-119">Эта команда возвращает все группы пользователей с именем 0123456789.</span><span class="sxs-lookup"><span data-stu-id="b470b-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="b470b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b470b-120">PARAMETERS</span></span>

### <span data-ttu-id="b470b-121">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b470b-121">-Context</span></span>
<span data-ttu-id="b470b-122">Указывает экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b470b-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b470b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b470b-123">-DefaultProfile</span></span>
<span data-ttu-id="b470b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b470b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b470b-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b470b-125">-GroupId</span></span>
<span data-ttu-id="b470b-126">Определяет ИД группы.</span><span class="sxs-lookup"><span data-stu-id="b470b-126">Specifies the group ID.</span></span>
<span data-ttu-id="b470b-127">Если он задан, с помощью cmdlet можно найти группу по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="b470b-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b470b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b470b-128">-Name</span></span>
<span data-ttu-id="b470b-129">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="b470b-129">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b470b-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b470b-130">-ProductId</span></span>
<span data-ttu-id="b470b-131">Идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="b470b-131">Identifier of existing product.</span></span>
<span data-ttu-id="b470b-132">Если указано, будут возвращены все группы, которые были назначены продукту.</span><span class="sxs-lookup"><span data-stu-id="b470b-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="b470b-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b470b-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b470b-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="b470b-134">-UserId</span></span>
<span data-ttu-id="b470b-135">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="b470b-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="b470b-136">Если он задан, будет возвращены все группы, которые были назначены продукту.</span><span class="sxs-lookup"><span data-stu-id="b470b-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b470b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b470b-137">CommonParameters</span></span>
<span data-ttu-id="b470b-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b470b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b470b-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b470b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b470b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b470b-140">INPUTS</span></span>

### <span data-ttu-id="b470b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b470b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b470b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b470b-142">System.String</span></span>

## <span data-ttu-id="b470b-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b470b-143">OUTPUTS</span></span>

### <span data-ttu-id="b470b-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b470b-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="b470b-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b470b-145">NOTES</span></span>

## <span data-ttu-id="b470b-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b470b-146">RELATED LINKS</span></span>

[<span data-ttu-id="b470b-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b470b-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="b470b-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b470b-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="b470b-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b470b-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


