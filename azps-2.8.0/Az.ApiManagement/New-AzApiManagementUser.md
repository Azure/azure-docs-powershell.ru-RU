---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: d8d88c2071cafad33fd4a80cb4c2de63ccf89647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728019"
---
# <span data-ttu-id="0550a-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0550a-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="0550a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0550a-102">SYNOPSIS</span></span>
<span data-ttu-id="0550a-103">Регистрация нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-103">Registers a new user.</span></span>

## <span data-ttu-id="0550a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0550a-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0550a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0550a-105">DESCRIPTION</span></span>
<span data-ttu-id="0550a-106">Командлет **New-AzApiManagementUser** регистрирует нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="0550a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0550a-107">EXAMPLES</span></span>

### <span data-ttu-id="0550a-108">Пример 1: регистрация нового пользователя</span><span class="sxs-lookup"><span data-stu-id="0550a-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="0550a-109">Эта команда регистрирует нового пользователя с именем Patti Белова.</span><span class="sxs-lookup"><span data-stu-id="0550a-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="0550a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0550a-110">PARAMETERS</span></span>

### <span data-ttu-id="0550a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="0550a-111">-Context</span></span>
<span data-ttu-id="0550a-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0550a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0550a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0550a-113">-DefaultProfile</span></span>
<span data-ttu-id="0550a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0550a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0550a-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="0550a-115">-Email</span></span>
<span data-ttu-id="0550a-116">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="0550a-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="0550a-117">-FirstName</span></span>
<span data-ttu-id="0550a-118">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="0550a-119">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="0550a-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="0550a-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="0550a-120">-LastName</span></span>
<span data-ttu-id="0550a-121">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="0550a-122">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="0550a-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="0550a-123">-Примечание</span><span class="sxs-lookup"><span data-stu-id="0550a-123">-Note</span></span>
<span data-ttu-id="0550a-124">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="0550a-124">Specifies a note about the user.</span></span>
<span data-ttu-id="0550a-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0550a-125">This parameter is optional.</span></span>
<span data-ttu-id="0550a-126">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0550a-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="0550a-127">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="0550a-127">-Password</span></span>
<span data-ttu-id="0550a-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-128">Specifies the user password.</span></span>
<span data-ttu-id="0550a-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0550a-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0550a-130">-State</span><span class="sxs-lookup"><span data-stu-id="0550a-130">-State</span></span>
<span data-ttu-id="0550a-131">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-131">Specifies the user state.</span></span>
<span data-ttu-id="0550a-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0550a-132">This parameter is optional.</span></span>
<span data-ttu-id="0550a-133">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0550a-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0550a-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="0550a-134">-UserId</span></span>
<span data-ttu-id="0550a-135">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-135">Specifies the user ID.</span></span>
<span data-ttu-id="0550a-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="0550a-136">This parameter is optional.</span></span>
<span data-ttu-id="0550a-137">Если этот параметр не указан, этот командлет создает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="0550a-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="0550a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0550a-138">CommonParameters</span></span>
<span data-ttu-id="0550a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0550a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0550a-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0550a-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0550a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0550a-141">INPUTS</span></span>

### <span data-ttu-id="0550a-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0550a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0550a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0550a-143">System.String</span></span>

### <span data-ttu-id="0550a-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0550a-144">System.Security.SecureString</span></span>

### <span data-ttu-id="0550a-145">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementUserState, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="0550a-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0550a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0550a-146">OUTPUTS</span></span>

### <span data-ttu-id="0550a-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0550a-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="0550a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0550a-148">NOTES</span></span>

## <span data-ttu-id="0550a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0550a-149">RELATED LINKS</span></span>

[<span data-ttu-id="0550a-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0550a-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="0550a-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="0550a-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


