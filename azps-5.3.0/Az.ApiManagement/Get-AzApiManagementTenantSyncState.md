---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516533"
---
# <span data-ttu-id="37293-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="37293-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="37293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37293-102">SYNOPSIS</span></span>
<span data-ttu-id="37293-103">Возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="37293-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="37293-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="37293-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37293-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37293-105">DESCRIPTION</span></span>
<span data-ttu-id="37293-106">Командалет **Get-AzApiManagementTenantSyncState** получает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="37293-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="37293-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="37293-107">EXAMPLES</span></span>

### <span data-ttu-id="37293-108">Пример 1. Просмотр состояния последней синхронизации</span><span class="sxs-lookup"><span data-stu-id="37293-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="37293-109">Эта команда получает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="37293-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="37293-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37293-110">PARAMETERS</span></span>

### <span data-ttu-id="37293-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="37293-111">-Context</span></span>
<span data-ttu-id="37293-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="37293-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="37293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37293-113">-DefaultProfile</span></span>
<span data-ttu-id="37293-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37293-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37293-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37293-115">CommonParameters</span></span>
<span data-ttu-id="37293-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37293-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37293-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37293-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37293-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37293-118">INPUTS</span></span>

### <span data-ttu-id="37293-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="37293-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="37293-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37293-120">OUTPUTS</span></span>

### <span data-ttu-id="37293-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="37293-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="37293-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="37293-122">NOTES</span></span>

## <span data-ttu-id="37293-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37293-123">RELATED LINKS</span></span>
