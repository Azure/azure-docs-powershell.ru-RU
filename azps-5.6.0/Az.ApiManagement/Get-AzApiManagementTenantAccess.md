---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c19888bd45ae943b60b90172913a83f42a1fd6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004931"
---
# <span data-ttu-id="3d748-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="3d748-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="3d748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d748-102">SYNOPSIS</span></span>
<span data-ttu-id="3d748-103">Получает конфигурацию доступа для клиента.</span><span class="sxs-lookup"><span data-stu-id="3d748-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="3d748-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d748-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d748-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d748-105">DESCRIPTION</span></span>
<span data-ttu-id="3d748-106">С **его учетом** можно получить конфигурацию доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="3d748-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="3d748-107">Ключи не включаются в сведения о результатах.</span><span class="sxs-lookup"><span data-stu-id="3d748-107">Keys will not be included into result details.</span></span> <span data-ttu-id="3d748-108">Чтобы получить секрет клиента, используйте **Get-AzApiManagementTenantAccessSecret.**</span><span class="sxs-lookup"><span data-stu-id="3d748-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="3d748-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d748-109">EXAMPLES</span></span>

### <span data-ttu-id="3d748-110">Пример 1. Настройка доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="3d748-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="3d748-111">Эта команда получает конфигурацию доступа клиента для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="3d748-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="3d748-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d748-112">PARAMETERS</span></span>

### <span data-ttu-id="3d748-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="3d748-113">-Context</span></span>
<span data-ttu-id="3d748-114">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="3d748-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3d748-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d748-115">-DefaultProfile</span></span>
<span data-ttu-id="3d748-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d748-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d748-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d748-117">CommonParameters</span></span>
<span data-ttu-id="3d748-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d748-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d748-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d748-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d748-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d748-120">INPUTS</span></span>

### <span data-ttu-id="3d748-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3d748-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="3d748-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d748-122">OUTPUTS</span></span>

### <span data-ttu-id="3d748-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="3d748-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="3d748-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d748-124">NOTES</span></span>

## <span data-ttu-id="3d748-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d748-125">RELATED LINKS</span></span>

[<span data-ttu-id="3d748-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="3d748-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


