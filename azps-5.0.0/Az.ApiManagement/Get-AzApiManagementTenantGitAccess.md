---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247946"
---
# <span data-ttu-id="9b86f-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="9b86f-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="9b86f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b86f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b86f-103">Возвращает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="9b86f-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="9b86f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b86f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b86f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b86f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b86f-106">Командлет **Get-AzApiManagementTenantGitAccess** получает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="9b86f-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="9b86f-107">Ключи не будут включены в данные результата.</span><span class="sxs-lookup"><span data-stu-id="9b86f-107">Keys will not be included into result details.</span></span> <span data-ttu-id="9b86f-108">Чтобы получить секрет клиента, используйте **Get-AzApiManagementTenantGitAccessSecret**.</span><span class="sxs-lookup"><span data-stu-id="9b86f-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="9b86f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b86f-109">EXAMPLES</span></span>

### <span data-ttu-id="9b86f-110">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="9b86f-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="9b86f-111">Эта команда возвращает конфигурацию доступа Git для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="9b86f-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="9b86f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b86f-112">PARAMETERS</span></span>

### <span data-ttu-id="9b86f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="9b86f-113">-Context</span></span>
<span data-ttu-id="9b86f-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9b86f-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b86f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b86f-115">-DefaultProfile</span></span>
<span data-ttu-id="9b86f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b86f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b86f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b86f-117">CommonParameters</span></span>
<span data-ttu-id="9b86f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b86f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b86f-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b86f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b86f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b86f-120">INPUTS</span></span>

### <span data-ttu-id="9b86f-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b86f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="9b86f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b86f-122">OUTPUTS</span></span>

### <span data-ttu-id="9b86f-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="9b86f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="9b86f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b86f-124">NOTES</span></span>

## <span data-ttu-id="9b86f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b86f-125">RELATED LINKS</span></span>