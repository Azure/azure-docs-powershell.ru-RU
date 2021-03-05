---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: b4c89a1f0da5e4ce07d9d2174fce031365e09cb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979075"
---
# <span data-ttu-id="f55ab-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f55ab-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="f55ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f55ab-103">Создает URL-адрес SSO для пользователя.</span><span class="sxs-lookup"><span data-stu-id="f55ab-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="f55ab-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f55ab-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55ab-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f55ab-105">DESCRIPTION</span></span>
<span data-ttu-id="f55ab-106">Для пользователя с его учетной записи создается URL-адрес для единого входов **.AzApiManagementUserSoUrl.**</span><span class="sxs-lookup"><span data-stu-id="f55ab-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="f55ab-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f55ab-107">EXAMPLES</span></span>

### <span data-ttu-id="f55ab-108">Пример 1. Получите URL-адрес SSO пользователя</span><span class="sxs-lookup"><span data-stu-id="f55ab-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f55ab-109">Эта команда получает URL-адрес SSO пользователя.</span><span class="sxs-lookup"><span data-stu-id="f55ab-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="f55ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f55ab-110">PARAMETERS</span></span>

### <span data-ttu-id="f55ab-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="f55ab-111">-Context</span></span>
<span data-ttu-id="f55ab-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f55ab-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f55ab-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="f55ab-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f55ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55ab-114">-DefaultProfile</span></span>
<span data-ttu-id="f55ab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f55ab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f55ab-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="f55ab-116">-UserId</span></span>
<span data-ttu-id="f55ab-117">Определяет ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="f55ab-117">Specifies a user ID.</span></span>
<span data-ttu-id="f55ab-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="f55ab-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f55ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55ab-119">CommonParameters</span></span>
<span data-ttu-id="f55ab-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55ab-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f55ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55ab-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f55ab-122">INPUTS</span></span>

### <span data-ttu-id="f55ab-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f55ab-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f55ab-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f55ab-124">System.String</span></span>

## <span data-ttu-id="f55ab-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f55ab-125">OUTPUTS</span></span>

### <span data-ttu-id="f55ab-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f55ab-126">System.String</span></span>

## <span data-ttu-id="f55ab-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f55ab-127">NOTES</span></span>

## <span data-ttu-id="f55ab-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f55ab-128">RELATED LINKS</span></span>

[<span data-ttu-id="f55ab-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f55ab-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


