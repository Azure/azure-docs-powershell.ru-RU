---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566343"
---
# <span data-ttu-id="a0781-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0781-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="a0781-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a0781-102">SYNOPSIS</span></span>
<span data-ttu-id="a0781-103">Регистрация нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0781-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a0781-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0781-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0781-105">DESCRIPTION</span></span>
<span data-ttu-id="a0781-106">Командлет **New-AzureRmApiManagementUser** регистрирует нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="a0781-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a0781-107">EXAMPLES</span></span>

### <span data-ttu-id="a0781-108">Пример 1: регистрация нового пользователя</span><span class="sxs-lookup"><span data-stu-id="a0781-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="a0781-109">Эта команда регистрирует нового пользователя с именем Patti Белова.</span><span class="sxs-lookup"><span data-stu-id="a0781-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="a0781-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a0781-110">PARAMETERS</span></span>

### <span data-ttu-id="a0781-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a0781-111">-Context</span></span>
<span data-ttu-id="a0781-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a0781-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a0781-113">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="a0781-113">-Email</span></span>
<span data-ttu-id="a0781-114">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="a0781-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a0781-115">-FirstName</span></span>
<span data-ttu-id="a0781-116">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="a0781-117">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="a0781-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="a0781-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="a0781-118">-LastName</span></span>
<span data-ttu-id="a0781-119">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="a0781-120">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="a0781-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="a0781-121">-Примечание</span><span class="sxs-lookup"><span data-stu-id="a0781-121">-Note</span></span>
<span data-ttu-id="a0781-122">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="a0781-122">Specifies a note about the user.</span></span>
<span data-ttu-id="a0781-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a0781-123">This parameter is optional.</span></span>
<span data-ttu-id="a0781-124">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="a0781-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="a0781-125">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="a0781-125">-Password</span></span>
<span data-ttu-id="a0781-126">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-126">Specifies the user password.</span></span>
<span data-ttu-id="a0781-127">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a0781-127">This parameter is required.</span></span>

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

### <span data-ttu-id="a0781-128">-State</span><span class="sxs-lookup"><span data-stu-id="a0781-128">-State</span></span>
<span data-ttu-id="a0781-129">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-129">Specifies the user state.</span></span>
<span data-ttu-id="a0781-130">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a0781-130">This parameter is optional.</span></span>
<span data-ttu-id="a0781-131">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="a0781-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0781-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="a0781-132">-UserId</span></span>
<span data-ttu-id="a0781-133">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-133">Specifies the user ID.</span></span>
<span data-ttu-id="a0781-134">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="a0781-134">This parameter is optional.</span></span>
<span data-ttu-id="a0781-135">Если этот параметр не указан, этот командлет создает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="a0781-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="a0781-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0781-136">-DefaultProfile</span></span>
<span data-ttu-id="a0781-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a0781-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0781-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0781-138">CommonParameters</span></span>
<span data-ttu-id="a0781-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a0781-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0781-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0781-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0781-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a0781-141">INPUTS</span></span>

## <span data-ttu-id="a0781-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0781-142">OUTPUTS</span></span>

### <span data-ttu-id="a0781-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0781-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="a0781-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="a0781-144">NOTES</span></span>

## <span data-ttu-id="a0781-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0781-145">RELATED LINKS</span></span>

[<span data-ttu-id="a0781-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0781-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="a0781-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="a0781-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


