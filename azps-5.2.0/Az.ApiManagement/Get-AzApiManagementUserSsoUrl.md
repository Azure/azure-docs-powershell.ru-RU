---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392420"
---
# <span data-ttu-id="fc650-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="fc650-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="fc650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc650-102">SYNOPSIS</span></span>
<span data-ttu-id="fc650-103">Создает URL-адрес SSO для пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc650-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="fc650-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc650-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc650-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc650-105">DESCRIPTION</span></span>
<span data-ttu-id="fc650-106">Cmdlet **Get-AzApiManagementUserSerSoUrl** создает для пользователя единый URL-адрес для регистрации.</span><span class="sxs-lookup"><span data-stu-id="fc650-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="fc650-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc650-107">EXAMPLES</span></span>

### <span data-ttu-id="fc650-108">Пример 1. Получите URL-адрес SSO пользователя</span><span class="sxs-lookup"><span data-stu-id="fc650-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="fc650-109">Эта команда получает URL-адрес SSO пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc650-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="fc650-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc650-110">PARAMETERS</span></span>

### <span data-ttu-id="fc650-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="fc650-111">-Context</span></span>
<span data-ttu-id="fc650-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="fc650-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="fc650-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="fc650-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fc650-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc650-114">-DefaultProfile</span></span>
<span data-ttu-id="fc650-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc650-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc650-116">-UserId</span><span class="sxs-lookup"><span data-stu-id="fc650-116">-UserId</span></span>
<span data-ttu-id="fc650-117">Определяет ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc650-117">Specifies a user ID.</span></span>
<span data-ttu-id="fc650-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="fc650-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fc650-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc650-119">CommonParameters</span></span>
<span data-ttu-id="fc650-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc650-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc650-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc650-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc650-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc650-122">INPUTS</span></span>

### <span data-ttu-id="fc650-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fc650-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc650-124">System.String</span><span class="sxs-lookup"><span data-stu-id="fc650-124">System.String</span></span>

## <span data-ttu-id="fc650-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc650-125">OUTPUTS</span></span>

### <span data-ttu-id="fc650-126">System.String</span><span class="sxs-lookup"><span data-stu-id="fc650-126">System.String</span></span>

## <span data-ttu-id="fc650-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc650-127">NOTES</span></span>

## <span data-ttu-id="fc650-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc650-128">RELATED LINKS</span></span>

[<span data-ttu-id="fc650-129">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fc650-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


