---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315416"
---
# <span data-ttu-id="0d23e-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d23e-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="0d23e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d23e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d23e-103">Возвращает все или определенные группы управления API.</span><span class="sxs-lookup"><span data-stu-id="0d23e-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="0d23e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d23e-104">SYNTAX</span></span>

### <span data-ttu-id="0d23e-105">GetAllGroups (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d23e-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d23e-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="0d23e-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d23e-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="0d23e-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d23e-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="0d23e-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d23e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d23e-109">DESCRIPTION</span></span>
<span data-ttu-id="0d23e-110">Командлет **Get-AzApiManagementGroup** возвращает все или определенные группы управления API.</span><span class="sxs-lookup"><span data-stu-id="0d23e-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="0d23e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d23e-111">EXAMPLES</span></span>

### <span data-ttu-id="0d23e-112">Пример 1: получение всех групп</span><span class="sxs-lookup"><span data-stu-id="0d23e-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="0d23e-113">Эта команда возвращает все группы.</span><span class="sxs-lookup"><span data-stu-id="0d23e-113">This command gets all groups.</span></span>

### <span data-ttu-id="0d23e-114">Пример 2: получение учетной записи группы по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="0d23e-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="0d23e-115">Эта команда получает идентификатор группы с именем 0123456789.</span><span class="sxs-lookup"><span data-stu-id="0d23e-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="0d23e-116">Пример 3: получение группировки по имени</span><span class="sxs-lookup"><span data-stu-id="0d23e-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="0d23e-117">Эта команда возвращает группу с именем Group0002.</span><span class="sxs-lookup"><span data-stu-id="0d23e-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="0d23e-118">Пример 4: получение всех групп пользователей</span><span class="sxs-lookup"><span data-stu-id="0d23e-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0d23e-119">Эта команда получает все группы пользователей с ИДЕНТИФИКАТОРом пользователя 0123456789.</span><span class="sxs-lookup"><span data-stu-id="0d23e-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="0d23e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d23e-120">PARAMETERS</span></span>

### <span data-ttu-id="0d23e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0d23e-121">-Context</span></span>
<span data-ttu-id="0d23e-122">Указывает экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0d23e-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="0d23e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d23e-123">-DefaultProfile</span></span>
<span data-ttu-id="0d23e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d23e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d23e-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0d23e-125">-GroupId</span></span>
<span data-ttu-id="0d23e-126">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="0d23e-126">Specifies the group ID.</span></span>
<span data-ttu-id="0d23e-127">Если задано значение, командлет пытается найти группу по ее идентификатору.</span><span class="sxs-lookup"><span data-stu-id="0d23e-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="0d23e-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d23e-128">-Name</span></span>
<span data-ttu-id="0d23e-129">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="0d23e-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="0d23e-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0d23e-130">-ProductId</span></span>
<span data-ttu-id="0d23e-131">Идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="0d23e-131">Identifier of existing product.</span></span>
<span data-ttu-id="0d23e-132">Если задано значение, будет возвращено все группы, которым назначен продукт.</span><span class="sxs-lookup"><span data-stu-id="0d23e-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="0d23e-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0d23e-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="0d23e-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="0d23e-134">-UserId</span></span>
<span data-ttu-id="0d23e-135">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="0d23e-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="0d23e-136">Если указан командлет, вы вернете все группы, в которые назначен продукт.</span><span class="sxs-lookup"><span data-stu-id="0d23e-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="0d23e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d23e-137">CommonParameters</span></span>
<span data-ttu-id="0d23e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d23e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d23e-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d23e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d23e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d23e-140">INPUTS</span></span>

### <span data-ttu-id="0d23e-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d23e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d23e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0d23e-142">System.String</span></span>

## <span data-ttu-id="0d23e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d23e-143">OUTPUTS</span></span>

### <span data-ttu-id="0d23e-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d23e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="0d23e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d23e-145">NOTES</span></span>

## <span data-ttu-id="0d23e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d23e-146">RELATED LINKS</span></span>

[<span data-ttu-id="0d23e-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d23e-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="0d23e-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d23e-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="0d23e-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d23e-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


