---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565734"
---
# <span data-ttu-id="8afb2-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8afb2-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="8afb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8afb2-102">SYNOPSIS</span></span>
<span data-ttu-id="8afb2-103">Создает новый объект прокси-сервера в серверной части.</span><span class="sxs-lookup"><span data-stu-id="8afb2-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8afb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8afb2-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8afb2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8afb2-105">DESCRIPTION</span></span>
<span data-ttu-id="8afb2-106">Создает новый объект-посредник для базы данных, который может быть передан при создании новой серверной сущности.</span><span class="sxs-lookup"><span data-stu-id="8afb2-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="8afb2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8afb2-107">EXAMPLES</span></span>

### <span data-ttu-id="8afb2-108">Создание объекта прокси-сервера в серверной In-Memory</span><span class="sxs-lookup"><span data-stu-id="8afb2-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="8afb2-109">Создание объекта прокси-сервера в серверной части</span><span class="sxs-lookup"><span data-stu-id="8afb2-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="8afb2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8afb2-110">PARAMETERS</span></span>

### <span data-ttu-id="8afb2-111">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="8afb2-111">-Password</span></span>
<span data-ttu-id="8afb2-112">Пароль прокси-сервера, используемый для подключения к прокси-серверу внутренней сети.</span><span class="sxs-lookup"><span data-stu-id="8afb2-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="8afb2-113">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8afb2-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afb2-114">— URL-адрес</span><span class="sxs-lookup"><span data-stu-id="8afb2-114">-Url</span></span>
<span data-ttu-id="8afb2-115">Адрес прокси-сервера, который будет использоваться для переадресации звонков на сервер.</span><span class="sxs-lookup"><span data-stu-id="8afb2-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="8afb2-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8afb2-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afb2-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="8afb2-117">-UserName</span></span>
<span data-ttu-id="8afb2-118">Имя пользователя прокси-сервера, используемого для подключения к прокси-серверу.</span><span class="sxs-lookup"><span data-stu-id="8afb2-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="8afb2-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8afb2-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8afb2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8afb2-120">-DefaultProfile</span></span>
<span data-ttu-id="8afb2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8afb2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8afb2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afb2-122">CommonParameters</span></span>
<span data-ttu-id="8afb2-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8afb2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afb2-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8afb2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afb2-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8afb2-125">INPUTS</span></span>

## <span data-ttu-id="8afb2-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8afb2-126">OUTPUTS</span></span>

### <span data-ttu-id="8afb2-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="8afb2-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="8afb2-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8afb2-128">NOTES</span></span>

## <span data-ttu-id="8afb2-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8afb2-129">RELATED LINKS</span></span>

[<span data-ttu-id="8afb2-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8afb2-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="8afb2-131">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8afb2-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8afb2-132">New-AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="8afb2-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="8afb2-133">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8afb2-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="8afb2-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="8afb2-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
