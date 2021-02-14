---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210572"
---
# <span data-ttu-id="b315c-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b315c-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="b315c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b315c-102">SYNOPSIS</span></span>
<span data-ttu-id="b315c-103">Возвращает пользователя или пользователей.</span><span class="sxs-lookup"><span data-stu-id="b315c-103">Gets a user or users.</span></span>

## <span data-ttu-id="b315c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b315c-104">SYNTAX</span></span>

### <span data-ttu-id="b315c-105">GeAllUsers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b315c-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b315c-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="b315c-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b315c-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="b315c-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b315c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b315c-108">DESCRIPTION</span></span>
<span data-ttu-id="b315c-109">Для получения указанного пользователя (или всех пользователей), если он не указан, cmdlet **Get-AzApiManagementUser** получает указанного пользователя или всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="b315c-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="b315c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b315c-110">EXAMPLES</span></span>

### <span data-ttu-id="b315c-111">Пример 1. Получить всех пользователей</span><span class="sxs-lookup"><span data-stu-id="b315c-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="b315c-112">Эта команда позволяет поохить всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="b315c-112">This command gets all users.</span></span>

### <span data-ttu-id="b315c-113">Пример 2. Как получить пользователя по ИД</span><span class="sxs-lookup"><span data-stu-id="b315c-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="b315c-114">Эта команда возвращает пользователя по ИД.</span><span class="sxs-lookup"><span data-stu-id="b315c-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="b315c-115">Пример 3. Поимка пользователей по фамилиям</span><span class="sxs-lookup"><span data-stu-id="b315c-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="b315c-116">Эта команда возвращает пользователей с указанной фамилией (Fuller).</span><span class="sxs-lookup"><span data-stu-id="b315c-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="b315c-117">Пример 4. Как получить пользователя по адресу электронной почты</span><span class="sxs-lookup"><span data-stu-id="b315c-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="b315c-118">Эта команда возвращает пользователя, у который указан адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b315c-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="b315c-119">Пример 5. Получить всех пользователей в группе</span><span class="sxs-lookup"><span data-stu-id="b315c-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="b315c-120">Эта команда возвращает всех пользователей в указанной группе.</span><span class="sxs-lookup"><span data-stu-id="b315c-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="b315c-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b315c-121">PARAMETERS</span></span>

### <span data-ttu-id="b315c-122">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b315c-122">-Context</span></span>
<span data-ttu-id="b315c-123">Указывает экземпляр **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="b315c-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="b315c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b315c-124">-DefaultProfile</span></span>
<span data-ttu-id="b315c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b315c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b315c-126">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="b315c-126">-Email</span></span>
<span data-ttu-id="b315c-127">Определяет адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="b315c-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="b315c-128">Если этот параметр задан, этот cmdlet находит пользователя по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="b315c-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="b315c-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b315c-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b315c-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="b315c-130">-FirstName</span></span>
<span data-ttu-id="b315c-131">Указывает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="b315c-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="b315c-132">Если этот параметр задан, этот cmdlet находит пользователя по имени.</span><span class="sxs-lookup"><span data-stu-id="b315c-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="b315c-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b315c-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b315c-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b315c-134">-GroupId</span></span>
<span data-ttu-id="b315c-135">Идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="b315c-135">Specifies the group identifier.</span></span>
<span data-ttu-id="b315c-136">Если он задан, этот cmdlet находит всех пользователей в указанной группе.</span><span class="sxs-lookup"><span data-stu-id="b315c-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="b315c-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b315c-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b315c-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="b315c-138">-LastName</span></span>
<span data-ttu-id="b315c-139">Указывает фамилию пользователя.</span><span class="sxs-lookup"><span data-stu-id="b315c-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="b315c-140">Если он задан, этот cmdlet находит пользователей по фамилиям.</span><span class="sxs-lookup"><span data-stu-id="b315c-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="b315c-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b315c-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b315c-142">-State</span><span class="sxs-lookup"><span data-stu-id="b315c-142">-State</span></span>
<span data-ttu-id="b315c-143">Определяет состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="b315c-143">Specifies the user state.</span></span>
<span data-ttu-id="b315c-144">Если он задан, этот cmdlet находит пользователей в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="b315c-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="b315c-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b315c-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b315c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="b315c-146">-UserId</span></span>
<span data-ttu-id="b315c-147">Определяет ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="b315c-147">Specifies a user ID.</span></span>
<span data-ttu-id="b315c-148">Если он задан, этот cmdlet находит пользователя по этому идентификатору.</span><span class="sxs-lookup"><span data-stu-id="b315c-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="b315c-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b315c-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="b315c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b315c-150">CommonParameters</span></span>
<span data-ttu-id="b315c-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b315c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b315c-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b315c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b315c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b315c-153">INPUTS</span></span>

### <span data-ttu-id="b315c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b315c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b315c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b315c-155">System.String</span></span>

### <span data-ttu-id="b315c-156">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b315c-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b315c-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b315c-157">OUTPUTS</span></span>

### <span data-ttu-id="b315c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b315c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="b315c-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b315c-159">NOTES</span></span>

## <span data-ttu-id="b315c-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b315c-160">RELATED LINKS</span></span>

[<span data-ttu-id="b315c-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b315c-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="b315c-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b315c-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="b315c-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b315c-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


