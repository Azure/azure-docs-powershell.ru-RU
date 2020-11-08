---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078011"
---
# <span data-ttu-id="ceb3a-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ceb3a-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="ceb3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ceb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb3a-103">Возвращает пользователя или пользователей.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-103">Gets a user or users.</span></span>

## <span data-ttu-id="ceb3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ceb3a-104">SYNTAX</span></span>

### <span data-ttu-id="ceb3a-105">GeAllUsers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ceb3a-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ceb3a-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ceb3a-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ceb3a-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="ceb3a-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ceb3a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceb3a-108">DESCRIPTION</span></span>
<span data-ttu-id="ceb3a-109">Командлет **Get-AzApiManagementUser** получает указанного пользователя или всех пользователей, если не указан ни один пользователь.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="ceb3a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ceb3a-110">EXAMPLES</span></span>

### <span data-ttu-id="ceb3a-111">Пример 1: получение всех пользователей</span><span class="sxs-lookup"><span data-stu-id="ceb3a-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="ceb3a-112">Эта команда получает доступ ко всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-112">This command gets all users.</span></span>

### <span data-ttu-id="ceb3a-113">Пример 2: получение учетной записи пользователя с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="ceb3a-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ceb3a-114">Эта команда получает пользователя по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="ceb3a-115">Пример 3: получение имен пользователей по фамилии</span><span class="sxs-lookup"><span data-stu-id="ceb3a-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="ceb3a-116">Эта команда возвращает пользователей с указанными фамилиями (Беловом).</span><span class="sxs-lookup"><span data-stu-id="ceb3a-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="ceb3a-117">Пример 4: получение учетной записи пользователя по адресу электронной почты</span><span class="sxs-lookup"><span data-stu-id="ceb3a-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="ceb3a-118">Эта команда получает пользователя, у которого есть указанный адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="ceb3a-119">Пример 5: получение всех пользователей в группе</span><span class="sxs-lookup"><span data-stu-id="ceb3a-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="ceb3a-120">Эта команда получает всех пользователей в указанной группе.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="ceb3a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ceb3a-121">PARAMETERS</span></span>

### <span data-ttu-id="ceb3a-122">-Context</span><span class="sxs-lookup"><span data-stu-id="ceb3a-122">-Context</span></span>
<span data-ttu-id="ceb3a-123">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ceb3a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceb3a-124">-DefaultProfile</span></span>
<span data-ttu-id="ceb3a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceb3a-126">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="ceb3a-126">-Email</span></span>
<span data-ttu-id="ceb3a-127">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="ceb3a-128">Если указан этот параметр, этот командлет находит пользователя по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="ceb3a-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="ceb3a-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ceb3a-130">-FirstName</span></span>
<span data-ttu-id="ceb3a-131">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="ceb3a-132">Если указан этот параметр, этот командлет находит пользователя по имени.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="ceb3a-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="ceb3a-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ceb3a-134">-GroupId</span></span>
<span data-ttu-id="ceb3a-135">Указывает идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-135">Specifies the group identifier.</span></span>
<span data-ttu-id="ceb3a-136">Если указан, этот командлет находит всех пользователей в указанной группе.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="ceb3a-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="ceb3a-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="ceb3a-138">-LastName</span></span>
<span data-ttu-id="ceb3a-139">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="ceb3a-140">Если задано, этот командлет находит пользователей по фамилии.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="ceb3a-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="ceb3a-142">-State</span><span class="sxs-lookup"><span data-stu-id="ceb3a-142">-State</span></span>
<span data-ttu-id="ceb3a-143">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-143">Specifies the user state.</span></span>
<span data-ttu-id="ceb3a-144">Если задано, этот командлет находит пользователей в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="ceb3a-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="ceb3a-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="ceb3a-146">-UserId</span></span>
<span data-ttu-id="ceb3a-147">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-147">Specifies a user ID.</span></span>
<span data-ttu-id="ceb3a-148">Если он указан, этот командлет находит пользователя по этому идентификатору.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="ceb3a-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="ceb3a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb3a-150">CommonParameters</span></span>
<span data-ttu-id="ceb3a-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ceb3a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb3a-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ceb3a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb3a-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ceb3a-153">INPUTS</span></span>

### <span data-ttu-id="ceb3a-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ceb3a-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ceb3a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ceb3a-155">System.String</span></span>

### <span data-ttu-id="ceb3a-156">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementUserState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ceb3a-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ceb3a-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ceb3a-157">OUTPUTS</span></span>

### <span data-ttu-id="ceb3a-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ceb3a-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="ceb3a-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="ceb3a-159">NOTES</span></span>

## <span data-ttu-id="ceb3a-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ceb3a-160">RELATED LINKS</span></span>

[<span data-ttu-id="ceb3a-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ceb3a-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="ceb3a-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ceb3a-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="ceb3a-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ceb3a-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


