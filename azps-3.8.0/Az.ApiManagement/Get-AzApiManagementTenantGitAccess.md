---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: d9b179ab65fa4d081fd0d065d08dab42f8aee810
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072852"
---
# <span data-ttu-id="a5533-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="a5533-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="a5533-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5533-102">SYNOPSIS</span></span>
<span data-ttu-id="a5533-103">Возвращает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="a5533-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="a5533-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5533-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5533-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5533-105">DESCRIPTION</span></span>
<span data-ttu-id="a5533-106">Командлет **Get-AzApiManagementTenantGitAccess** получает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="a5533-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="a5533-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5533-107">EXAMPLES</span></span>

### <span data-ttu-id="a5533-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="a5533-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="a5533-109">Эта команда возвращает конфигурацию доступа Git для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="a5533-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="a5533-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5533-110">PARAMETERS</span></span>

### <span data-ttu-id="a5533-111">-Context</span><span class="sxs-lookup"><span data-stu-id="a5533-111">-Context</span></span>
<span data-ttu-id="a5533-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a5533-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a5533-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5533-113">-DefaultProfile</span></span>
<span data-ttu-id="a5533-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5533-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5533-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5533-115">CommonParameters</span></span>
<span data-ttu-id="a5533-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5533-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5533-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5533-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5533-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5533-118">INPUTS</span></span>

### <span data-ttu-id="a5533-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a5533-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="a5533-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5533-120">OUTPUTS</span></span>

### <span data-ttu-id="a5533-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="a5533-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a5533-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5533-122">NOTES</span></span>

## <span data-ttu-id="a5533-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5533-123">RELATED LINKS</span></span>
