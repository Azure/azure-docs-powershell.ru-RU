---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004872"
---
# <span data-ttu-id="82172-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="82172-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="82172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82172-102">SYNOPSIS</span></span>
<span data-ttu-id="82172-103">Получает ключи конфигурации доступа GIT для клиента.</span><span class="sxs-lookup"><span data-stu-id="82172-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="82172-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82172-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82172-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82172-105">DESCRIPTION</span></span>
<span data-ttu-id="82172-106">Получает ключи конфигурации доступа GIT для клиента.</span><span class="sxs-lookup"><span data-stu-id="82172-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="82172-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82172-107">EXAMPLES</span></span>

### <span data-ttu-id="82172-108">Пример 1. Настройка доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="82172-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="82172-109">Эта команда получает ключи конфигурации доступа GIT для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="82172-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="82172-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82172-110">PARAMETERS</span></span>

### <span data-ttu-id="82172-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="82172-111">-Context</span></span>
<span data-ttu-id="82172-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="82172-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="82172-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="82172-113">This parameter is required.</span></span>

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

### <span data-ttu-id="82172-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82172-114">-DefaultProfile</span></span>
<span data-ttu-id="82172-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82172-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82172-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82172-116">CommonParameters</span></span>
<span data-ttu-id="82172-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82172-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82172-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82172-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82172-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82172-119">INPUTS</span></span>

### <span data-ttu-id="82172-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82172-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="82172-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82172-121">OUTPUTS</span></span>

### <span data-ttu-id="82172-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="82172-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="82172-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82172-123">NOTES</span></span>

## <span data-ttu-id="82172-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82172-124">RELATED LINKS</span></span>
