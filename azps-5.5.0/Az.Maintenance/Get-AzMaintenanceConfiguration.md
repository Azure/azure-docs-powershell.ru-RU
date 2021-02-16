---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241304"
---
# <span data-ttu-id="6557b-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6557b-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="6557b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6557b-102">SYNOPSIS</span></span>
<span data-ttu-id="6557b-103">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="6557b-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="6557b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6557b-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6557b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6557b-105">DESCRIPTION</span></span>
<span data-ttu-id="6557b-106">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="6557b-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="6557b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6557b-107">EXAMPLES</span></span>

### <span data-ttu-id="6557b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6557b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="6557b-109">Получить запись конфигурации обслуживания</span><span class="sxs-lookup"><span data-stu-id="6557b-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="6557b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6557b-110">PARAMETERS</span></span>

### <span data-ttu-id="6557b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6557b-111">-DefaultProfile</span></span>
<span data-ttu-id="6557b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6557b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6557b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6557b-113">-Name</span></span>
<span data-ttu-id="6557b-114">Имя конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6557b-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6557b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6557b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6557b-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6557b-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6557b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6557b-117">CommonParameters</span></span>
<span data-ttu-id="6557b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6557b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6557b-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6557b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6557b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6557b-120">INPUTS</span></span>

### <span data-ttu-id="6557b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6557b-121">System.String</span></span>

## <span data-ttu-id="6557b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6557b-122">OUTPUTS</span></span>

### <span data-ttu-id="6557b-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="6557b-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="6557b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6557b-124">NOTES</span></span>

## <span data-ttu-id="6557b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6557b-125">RELATED LINKS</span></span>
