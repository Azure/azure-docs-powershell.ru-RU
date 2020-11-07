---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: 2a7a4d602b8e316377496af8ccb9c119338a5c99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720130"
---
# <span data-ttu-id="f5205-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f5205-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="f5205-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5205-102">SYNOPSIS</span></span>
<span data-ttu-id="f5205-103">Создание URL-адреса SSO для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5205-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="f5205-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5205-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5205-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5205-105">DESCRIPTION</span></span>
<span data-ttu-id="f5205-106">Командлет **Get-AzApiManagementUserSsoUrl** создает для пользователя URL-адрес единого входа.</span><span class="sxs-lookup"><span data-stu-id="f5205-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="f5205-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5205-107">EXAMPLES</span></span>

### <span data-ttu-id="f5205-108">Пример 1: получение URL-адреса пользователя для единого входа</span><span class="sxs-lookup"><span data-stu-id="f5205-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f5205-109">Эта команда получает URL-адрес пользователя SSO.</span><span class="sxs-lookup"><span data-stu-id="f5205-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="f5205-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5205-110">PARAMETERS</span></span>

### <span data-ttu-id="f5205-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f5205-111">-Context</span></span>
<span data-ttu-id="f5205-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f5205-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f5205-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f5205-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f5205-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5205-114">-DefaultProfile</span></span>
<span data-ttu-id="f5205-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5205-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5205-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="f5205-116">-UserId</span></span>
<span data-ttu-id="f5205-117">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="f5205-117">Specifies a user ID.</span></span>
<span data-ttu-id="f5205-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f5205-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f5205-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5205-119">CommonParameters</span></span>
<span data-ttu-id="f5205-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5205-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5205-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5205-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5205-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5205-122">INPUTS</span></span>

### <span data-ttu-id="f5205-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f5205-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f5205-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f5205-124">System.String</span></span>

## <span data-ttu-id="f5205-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5205-125">OUTPUTS</span></span>

### <span data-ttu-id="f5205-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f5205-126">System.String</span></span>

## <span data-ttu-id="f5205-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5205-127">NOTES</span></span>

## <span data-ttu-id="f5205-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5205-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5205-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f5205-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


