---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568359"
---
# <span data-ttu-id="c4e56-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="c4e56-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="c4e56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4e56-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e56-103">Возвращает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="c4e56-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4e56-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4e56-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4e56-105">DESCRIPTION</span></span>
<span data-ttu-id="c4e56-106">Командлет **Get-AzureRmApiManagementTenantGitAccess** получает конфигурацию доступа Git для клиента.</span><span class="sxs-lookup"><span data-stu-id="c4e56-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="c4e56-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4e56-107">EXAMPLES</span></span>

### <span data-ttu-id="c4e56-108">Пример 1: получение конфигурации доступа клиента</span><span class="sxs-lookup"><span data-stu-id="c4e56-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="c4e56-109">Эта команда возвращает конфигурацию доступа Git для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="c4e56-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="c4e56-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4e56-110">PARAMETERS</span></span>

### <span data-ttu-id="c4e56-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c4e56-111">-Context</span></span>
<span data-ttu-id="c4e56-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c4e56-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c4e56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e56-113">-DefaultProfile</span></span>
<span data-ttu-id="c4e56-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4e56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e56-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e56-115">CommonParameters</span></span>
<span data-ttu-id="c4e56-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4e56-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e56-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e56-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e56-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4e56-118">INPUTS</span></span>

## <span data-ttu-id="c4e56-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4e56-119">OUTPUTS</span></span>

### <span data-ttu-id="c4e56-120">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="c4e56-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="c4e56-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4e56-121">NOTES</span></span>

## <span data-ttu-id="c4e56-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4e56-122">RELATED LINKS</span></span>

