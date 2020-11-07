---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 2fe14349b179634bf93050840271d4d4b6905b3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720134"
---
# <span data-ttu-id="19b24-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="19b24-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="19b24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19b24-102">SYNOPSIS</span></span>
<span data-ttu-id="19b24-103">Возвращает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="19b24-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="19b24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19b24-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19b24-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19b24-105">DESCRIPTION</span></span>
<span data-ttu-id="19b24-106">Командлет **Get-AzApiManagementTenantGitAccess** получает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="19b24-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="19b24-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19b24-107">EXAMPLES</span></span>

### <span data-ttu-id="19b24-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="19b24-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="19b24-109">Эта команда возвращает конфигурацию доступа Git для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="19b24-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="19b24-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19b24-110">PARAMETERS</span></span>

### <span data-ttu-id="19b24-111">-Context</span><span class="sxs-lookup"><span data-stu-id="19b24-111">-Context</span></span>
<span data-ttu-id="19b24-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="19b24-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="19b24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b24-113">-DefaultProfile</span></span>
<span data-ttu-id="19b24-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19b24-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b24-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b24-115">CommonParameters</span></span>
<span data-ttu-id="19b24-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19b24-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b24-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b24-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b24-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19b24-118">INPUTS</span></span>

### <span data-ttu-id="19b24-119">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="19b24-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="19b24-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19b24-120">OUTPUTS</span></span>

### <span data-ttu-id="19b24-121">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="19b24-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="19b24-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="19b24-122">NOTES</span></span>

## <span data-ttu-id="19b24-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19b24-123">RELATED LINKS</span></span>
