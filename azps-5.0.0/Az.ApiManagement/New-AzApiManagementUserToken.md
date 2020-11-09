---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 558d6567b20cc127732ddb24a4e4be9351848f58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249735"
---
# <span data-ttu-id="35cb9-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="35cb9-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="35cb9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="35cb9-103">Создание маркера общего доступа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="35cb9-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="35cb9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35cb9-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35cb9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="35cb9-106">Командлет **New-AzApiManagementUserToken** создает маркер общего доступа для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="35cb9-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="35cb9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="35cb9-108">Пример 1: создание маркера общего доступа для пользователя Git</span><span class="sxs-lookup"><span data-stu-id="35cb9-108">Example 1: Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="35cb9-109">Этот сценарий получает пользователя Git, настроенного в службе ApiManagement, и создает маркер общего доступа, используя первичный ключ, допустимый в течение 8 часов.</span><span class="sxs-lookup"><span data-stu-id="35cb9-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

### <span data-ttu-id="35cb9-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35cb9-110">Example 2</span></span>

<span data-ttu-id="35cb9-111">Создание маркера общего доступа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="35cb9-111">Generates a Shared Access Token for the User.</span></span> <span data-ttu-id="35cb9-112">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="35cb9-112">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementUserToken -Context <PsApiManagementContext> -Expiry <DateTime> -UserId <String>
```

## <span data-ttu-id="35cb9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35cb9-113">PARAMETERS</span></span>

### <span data-ttu-id="35cb9-114">-Context</span><span class="sxs-lookup"><span data-stu-id="35cb9-114">-Context</span></span>
<span data-ttu-id="35cb9-115">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="35cb9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="35cb9-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="35cb9-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35cb9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cb9-117">-DefaultProfile</span></span>
<span data-ttu-id="35cb9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35cb9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35cb9-119">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="35cb9-119">-Expiry</span></span>
<span data-ttu-id="35cb9-120">Истек срок действия маркера.</span><span class="sxs-lookup"><span data-stu-id="35cb9-120">Expiry of the Token.</span></span>
<span data-ttu-id="35cb9-121">Если не указано, срок действия маркера истекает через 8 часов.</span><span class="sxs-lookup"><span data-stu-id="35cb9-121">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="35cb9-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="35cb9-122">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35cb9-123">-KeyType</span><span class="sxs-lookup"><span data-stu-id="35cb9-123">-KeyType</span></span>
<span data-ttu-id="35cb9-124">Клавиша пользователя, используемая при формировании маркера.</span><span class="sxs-lookup"><span data-stu-id="35cb9-124">User Key to use when generating the Token.</span></span>
<span data-ttu-id="35cb9-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="35cb9-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35cb9-126">-UserId</span><span class="sxs-lookup"><span data-stu-id="35cb9-126">-UserId</span></span>
<span data-ttu-id="35cb9-127">Идентификатор существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="35cb9-127">Identifier of existing user.</span></span>
<span data-ttu-id="35cb9-128">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="35cb9-128">This parameter is required.</span></span>

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

### <span data-ttu-id="35cb9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cb9-129">CommonParameters</span></span>
<span data-ttu-id="35cb9-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35cb9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cb9-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35cb9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cb9-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35cb9-132">INPUTS</span></span>

### <span data-ttu-id="35cb9-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="35cb9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="35cb9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="35cb9-134">System.String</span></span>

### <span data-ttu-id="35cb9-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="35cb9-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="35cb9-136">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="35cb9-136">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="35cb9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35cb9-137">OUTPUTS</span></span>

### <span data-ttu-id="35cb9-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="35cb9-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="35cb9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="35cb9-139">NOTES</span></span>

## <span data-ttu-id="35cb9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35cb9-140">RELATED LINKS</span></span>