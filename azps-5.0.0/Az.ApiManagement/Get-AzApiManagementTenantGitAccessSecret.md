---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319379"
---
# <span data-ttu-id="08597-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="08597-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="08597-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08597-102">SYNOPSIS</span></span>
<span data-ttu-id="08597-103">Получает ключи конфигурации доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="08597-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="08597-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08597-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08597-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08597-105">DESCRIPTION</span></span>
<span data-ttu-id="08597-106">Получает ключи конфигурации доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="08597-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="08597-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08597-107">EXAMPLES</span></span>

### <span data-ttu-id="08597-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="08597-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="08597-109">Эта команда получает ключи конфигурации доступа Git для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="08597-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="08597-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08597-110">PARAMETERS</span></span>

### <span data-ttu-id="08597-111">-Context</span><span class="sxs-lookup"><span data-stu-id="08597-111">-Context</span></span>
<span data-ttu-id="08597-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="08597-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="08597-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="08597-113">This parameter is required.</span></span>

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

### <span data-ttu-id="08597-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08597-114">-DefaultProfile</span></span>
<span data-ttu-id="08597-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08597-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08597-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08597-116">CommonParameters</span></span>
<span data-ttu-id="08597-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08597-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08597-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08597-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08597-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08597-119">INPUTS</span></span>

### <span data-ttu-id="08597-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08597-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="08597-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08597-121">OUTPUTS</span></span>

### <span data-ttu-id="08597-122">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="08597-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="08597-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="08597-123">NOTES</span></span>

## <span data-ttu-id="08597-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08597-124">RELATED LINKS</span></span>
