---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212177"
---
# <span data-ttu-id="b9c17-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="b9c17-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="b9c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c17-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c17-103">Получает ключи конфигурации доступа GIT для клиента.</span><span class="sxs-lookup"><span data-stu-id="b9c17-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b9c17-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9c17-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c17-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9c17-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c17-106">Получает ключи конфигурации доступа GIT для клиента.</span><span class="sxs-lookup"><span data-stu-id="b9c17-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b9c17-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9c17-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c17-108">Пример 1. Настройка доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="b9c17-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="b9c17-109">Эта команда получает ключи конфигурации доступа GIT для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="b9c17-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="b9c17-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9c17-110">PARAMETERS</span></span>

### <span data-ttu-id="b9c17-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b9c17-111">-Context</span></span>
<span data-ttu-id="b9c17-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b9c17-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b9c17-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b9c17-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b9c17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c17-114">-DefaultProfile</span></span>
<span data-ttu-id="b9c17-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c17-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c17-116">CommonParameters</span></span>
<span data-ttu-id="b9c17-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c17-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c17-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9c17-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c17-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9c17-119">INPUTS</span></span>

### <span data-ttu-id="b9c17-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9c17-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b9c17-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9c17-121">OUTPUTS</span></span>

### <span data-ttu-id="b9c17-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b9c17-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b9c17-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9c17-123">NOTES</span></span>

## <span data-ttu-id="b9c17-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9c17-124">RELATED LINKS</span></span>
