---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 8f02b88115ec6dc415ecf6cf5464503d61778cca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565976"
---
# <span data-ttu-id="ade4c-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ade4c-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="ade4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ade4c-102">SYNOPSIS</span></span>
<span data-ttu-id="ade4c-103">Возвращает пользователя или пользователей.</span><span class="sxs-lookup"><span data-stu-id="ade4c-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ade4c-104">SYNTAX</span></span>

### <span data-ttu-id="ade4c-105">GeAllUsers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ade4c-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ade4c-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="ade4c-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ade4c-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="ade4c-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade4c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade4c-108">DESCRIPTION</span></span>
<span data-ttu-id="ade4c-109">Командлет **Get-AzureRmApiManagementUser** получает указанного пользователя или всех пользователей, если не указан ни один пользователь.</span><span class="sxs-lookup"><span data-stu-id="ade4c-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="ade4c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ade4c-110">EXAMPLES</span></span>

### <span data-ttu-id="ade4c-111">Пример 1: получение всех пользователей</span><span class="sxs-lookup"><span data-stu-id="ade4c-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="ade4c-112">Эта команда получает доступ ко всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="ade4c-112">This command gets all users.</span></span>

### <span data-ttu-id="ade4c-113">Пример 2: получение учетной записи пользователя с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="ade4c-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="ade4c-114">Эта команда получает пользователя по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="ade4c-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="ade4c-115">Пример: получение имен пользователей по фамилии</span><span class="sxs-lookup"><span data-stu-id="ade4c-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="ade4c-116">Эта команда возвращает пользователей с указанными фамилиями (Беловом).</span><span class="sxs-lookup"><span data-stu-id="ade4c-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="ade4c-117">Пример 4: получение учетной записи пользователя по адресу электронной почты</span><span class="sxs-lookup"><span data-stu-id="ade4c-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="ade4c-118">Эта команда получает пользователя, у которого есть указанный адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ade4c-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="ade4c-119">Пример 5: получение всех пользователей в группе</span><span class="sxs-lookup"><span data-stu-id="ade4c-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="ade4c-120">Эта команда получает всех пользователей в указанной группе.</span><span class="sxs-lookup"><span data-stu-id="ade4c-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="ade4c-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ade4c-121">PARAMETERS</span></span>

### <span data-ttu-id="ade4c-122">-Context</span><span class="sxs-lookup"><span data-stu-id="ade4c-122">-Context</span></span>
<span data-ttu-id="ade4c-123">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ade4c-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade4c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade4c-124">-DefaultProfile</span></span>
<span data-ttu-id="ade4c-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ade4c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ade4c-126">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="ade4c-126">-Email</span></span>
<span data-ttu-id="ade4c-127">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="ade4c-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="ade4c-128">Если указан этот параметр, этот командлет находит пользователя по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="ade4c-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="ade4c-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ade4c-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="ade4c-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="ade4c-130">-FirstName</span></span>
<span data-ttu-id="ade4c-131">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ade4c-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="ade4c-132">Если указан этот параметр, этот командлет находит пользователя по имени.</span><span class="sxs-lookup"><span data-stu-id="ade4c-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="ade4c-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ade4c-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="ade4c-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ade4c-134">-GroupId</span></span>
<span data-ttu-id="ade4c-135">Указывает идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="ade4c-135">Specifies the group identifier.</span></span>
<span data-ttu-id="ade4c-136">Если указан, этот командлет находит всех пользователей в указанной группе.</span><span class="sxs-lookup"><span data-stu-id="ade4c-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="ade4c-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ade4c-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="ade4c-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="ade4c-138">-LastName</span></span>
<span data-ttu-id="ade4c-139">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ade4c-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="ade4c-140">Если задано, этот командлет находит пользователей по фамилии.</span><span class="sxs-lookup"><span data-stu-id="ade4c-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="ade4c-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ade4c-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="ade4c-142">-State</span><span class="sxs-lookup"><span data-stu-id="ade4c-142">-State</span></span>
<span data-ttu-id="ade4c-143">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="ade4c-143">Specifies the user state.</span></span>
<span data-ttu-id="ade4c-144">Если задано, этот командлет находит пользователей в этом состоянии.</span><span class="sxs-lookup"><span data-stu-id="ade4c-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="ade4c-145">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ade4c-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="ade4c-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="ade4c-146">-UserId</span></span>
<span data-ttu-id="ade4c-147">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="ade4c-147">Specifies a user ID.</span></span>
<span data-ttu-id="ade4c-148">Если он указан, этот командлет находит пользователя по этому идентификатору.</span><span class="sxs-lookup"><span data-stu-id="ade4c-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="ade4c-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ade4c-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="ade4c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade4c-150">CommonParameters</span></span>
<span data-ttu-id="ade4c-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ade4c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade4c-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade4c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade4c-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ade4c-153">INPUTS</span></span>

### <span data-ttu-id="ade4c-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ade4c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ade4c-155">System. String</span><span class="sxs-lookup"><span data-stu-id="ade4c-155">System.String</span></span>

### <span data-ttu-id="ade4c-156">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserState, Microsoft. Azure. Commands. ApiManagement. ServiceManagement, Version = 6.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ade4c-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ade4c-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade4c-157">OUTPUTS</span></span>

### <span data-ttu-id="ade4c-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ade4c-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="ade4c-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="ade4c-159">NOTES</span></span>

## <span data-ttu-id="ade4c-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ade4c-160">RELATED LINKS</span></span>

[<span data-ttu-id="ade4c-161">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ade4c-161">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="ade4c-162">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ade4c-162">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="ade4c-163">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ade4c-163">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


