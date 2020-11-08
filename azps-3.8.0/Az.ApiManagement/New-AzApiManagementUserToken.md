---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 5b8c781380ced5ed174c094cf1ff66a8eb820309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066391"
---
# <span data-ttu-id="e00d0-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="e00d0-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="e00d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e00d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e00d0-103">Создание маркера общего доступа для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e00d0-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="e00d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e00d0-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e00d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e00d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e00d0-106">Командлет **New-AzApiManagementUserToken** создает маркер общего доступа для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="e00d0-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="e00d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e00d0-107">EXAMPLES</span></span>

### <span data-ttu-id="e00d0-108">Пример 1: создание маркера общего доступа для пользователя Git</span><span class="sxs-lookup"><span data-stu-id="e00d0-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="e00d0-109">Этот сценарий получает пользователя Git, настроенного в службе ApiManagement, и создает маркер общего доступа, используя первичный ключ, допустимый в течение 8 часов.</span><span class="sxs-lookup"><span data-stu-id="e00d0-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="e00d0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e00d0-110">PARAMETERS</span></span>

### <span data-ttu-id="e00d0-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e00d0-111">-Context</span></span>
<span data-ttu-id="e00d0-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e00d0-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e00d0-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e00d0-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e00d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00d0-114">-DefaultProfile</span></span>
<span data-ttu-id="e00d0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e00d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e00d0-116">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="e00d0-116">-Expiry</span></span>
<span data-ttu-id="e00d0-117">Истек срок действия маркера.</span><span class="sxs-lookup"><span data-stu-id="e00d0-117">Expiry of the Token.</span></span>
<span data-ttu-id="e00d0-118">Если не указано, срок действия маркера истекает через 8 часов.</span><span class="sxs-lookup"><span data-stu-id="e00d0-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="e00d0-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e00d0-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="e00d0-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="e00d0-120">-KeyType</span></span>
<span data-ttu-id="e00d0-121">Клавиша пользователя, используемая при формировании маркера.</span><span class="sxs-lookup"><span data-stu-id="e00d0-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="e00d0-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e00d0-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="e00d0-123">-UserId</span><span class="sxs-lookup"><span data-stu-id="e00d0-123">-UserId</span></span>
<span data-ttu-id="e00d0-124">Идентификатор существующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="e00d0-124">Identifier of existing user.</span></span>
<span data-ttu-id="e00d0-125">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e00d0-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e00d0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00d0-126">CommonParameters</span></span>
<span data-ttu-id="e00d0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e00d0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00d0-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e00d0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00d0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e00d0-129">INPUTS</span></span>

### <span data-ttu-id="e00d0-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e00d0-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e00d0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e00d0-131">System.String</span></span>

### <span data-ttu-id="e00d0-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserKeyType</span><span class="sxs-lookup"><span data-stu-id="e00d0-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="e00d0-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e00d0-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e00d0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e00d0-134">OUTPUTS</span></span>

### <span data-ttu-id="e00d0-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="e00d0-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="e00d0-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e00d0-136">NOTES</span></span>

## <span data-ttu-id="e00d0-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e00d0-137">RELATED LINKS</span></span>
