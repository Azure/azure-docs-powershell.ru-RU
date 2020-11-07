---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735129"
---
# <span data-ttu-id="6b2f4-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b2f4-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="6b2f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b2f4-103">Регистрация нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b2f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b2f4-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b2f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b2f4-105">DESCRIPTION</span></span>
<span data-ttu-id="6b2f4-106">Командлет **New-AzureRmApiManagementUser** регистрирует нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="6b2f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b2f4-107">EXAMPLES</span></span>

### <span data-ttu-id="6b2f4-108">Пример 1: регистрация нового пользователя</span><span class="sxs-lookup"><span data-stu-id="6b2f4-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="6b2f4-109">Эта команда регистрирует нового пользователя с именем Patti Белова.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="6b2f4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b2f4-110">PARAMETERS</span></span>

### <span data-ttu-id="6b2f4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6b2f4-111">-Context</span></span>
<span data-ttu-id="6b2f4-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6b2f4-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b2f4-113">-DefaultProfile</span></span>
<span data-ttu-id="6b2f4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="6b2f4-115">-Email</span></span>
<span data-ttu-id="6b2f4-116">Указывает адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-116">Specifies the email address of the user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="6b2f4-117">-FirstName</span></span>
<span data-ttu-id="6b2f4-118">Задает первое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="6b2f4-119">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="6b2f4-120">-LastName</span></span>
<span data-ttu-id="6b2f4-121">Задает Последнее имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="6b2f4-122">Этот параметр должен содержать от 1 до 100 символов.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-123">-Примечание</span><span class="sxs-lookup"><span data-stu-id="6b2f4-123">-Note</span></span>
<span data-ttu-id="6b2f4-124">Указывает заметку о пользователе.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-124">Specifies a note about the user.</span></span>
<span data-ttu-id="6b2f4-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-125">This parameter is optional.</span></span>
<span data-ttu-id="6b2f4-126">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-126">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-127">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="6b2f4-127">-Password</span></span>
<span data-ttu-id="6b2f4-128">Указывает пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-128">Specifies the user password.</span></span>
<span data-ttu-id="6b2f4-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-130">-State</span><span class="sxs-lookup"><span data-stu-id="6b2f4-130">-State</span></span>
<span data-ttu-id="6b2f4-131">Указывает состояние пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-131">Specifies the user state.</span></span>
<span data-ttu-id="6b2f4-132">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-132">This parameter is optional.</span></span>
<span data-ttu-id="6b2f4-133">Значение этого параметра по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="6b2f4-134">-UserId</span></span>
<span data-ttu-id="6b2f4-135">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-135">Specifies the user ID.</span></span>
<span data-ttu-id="6b2f4-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-136">This parameter is optional.</span></span>
<span data-ttu-id="6b2f4-137">Если этот параметр не указан, этот командлет создает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b2f4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b2f4-138">CommonParameters</span></span>
<span data-ttu-id="6b2f4-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b2f4-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b2f4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b2f4-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b2f4-141">INPUTS</span></span>

### <span data-ttu-id="6b2f4-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="6b2f4-142">None</span></span>
<span data-ttu-id="6b2f4-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6b2f4-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b2f4-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b2f4-144">OUTPUTS</span></span>

### <span data-ttu-id="6b2f4-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b2f4-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="6b2f4-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b2f4-146">NOTES</span></span>

## <span data-ttu-id="6b2f4-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b2f4-147">RELATED LINKS</span></span>

[<span data-ttu-id="6b2f4-148">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b2f4-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="6b2f4-149">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6b2f4-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


