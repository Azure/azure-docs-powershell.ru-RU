---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226577"
---
# <span data-ttu-id="d4a0d-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="d4a0d-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="d4a0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a0d-103">Возвращает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="d4a0d-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="d4a0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4a0d-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a0d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4a0d-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a0d-106">Командалет **Get-AzApiManagementTenantSyncState** получает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="d4a0d-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="d4a0d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4a0d-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a0d-108">Пример 1. Просмотр состояния последней синхронизации</span><span class="sxs-lookup"><span data-stu-id="d4a0d-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="d4a0d-109">Эта команда получает состояние последней синхронизации между базой данных конфигурации и репозиторием Git.</span><span class="sxs-lookup"><span data-stu-id="d4a0d-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="d4a0d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4a0d-110">PARAMETERS</span></span>

### <span data-ttu-id="d4a0d-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d4a0d-111">-Context</span></span>
<span data-ttu-id="d4a0d-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d4a0d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d4a0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a0d-113">-DefaultProfile</span></span>
<span data-ttu-id="d4a0d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a0d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a0d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a0d-115">CommonParameters</span></span>
<span data-ttu-id="d4a0d-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a0d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a0d-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4a0d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a0d-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a0d-118">INPUTS</span></span>

### <span data-ttu-id="d4a0d-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4a0d-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="d4a0d-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a0d-120">OUTPUTS</span></span>

### <span data-ttu-id="d4a0d-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="d4a0d-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="d4a0d-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4a0d-122">NOTES</span></span>

## <span data-ttu-id="d4a0d-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4a0d-123">RELATED LINKS</span></span>
