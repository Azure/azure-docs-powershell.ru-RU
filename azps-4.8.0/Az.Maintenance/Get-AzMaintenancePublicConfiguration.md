---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236117"
---
# <span data-ttu-id="46ff7-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ff7-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="46ff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="46ff7-103">Получить запись конфигурации публичного обслуживания</span><span class="sxs-lookup"><span data-stu-id="46ff7-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="46ff7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46ff7-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ff7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="46ff7-106">Получить запись конфигурации публичного обслуживания</span><span class="sxs-lookup"><span data-stu-id="46ff7-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="46ff7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="46ff7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46ff7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="46ff7-109">Получить запись конфигурации публичного обслуживания</span><span class="sxs-lookup"><span data-stu-id="46ff7-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="46ff7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46ff7-110">PARAMETERS</span></span>

### <span data-ttu-id="46ff7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ff7-111">-DefaultProfile</span></span>
<span data-ttu-id="46ff7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46ff7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46ff7-113">-Name</span></span>
<span data-ttu-id="46ff7-114">Имя общедоступной конфигурации обслуживания.</span><span class="sxs-lookup"><span data-stu-id="46ff7-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ff7-115">-ResourceGroupName</span></span>
<span data-ttu-id="46ff7-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46ff7-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ff7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ff7-117">CommonParameters</span></span>
<span data-ttu-id="46ff7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46ff7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ff7-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46ff7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ff7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46ff7-120">INPUTS</span></span>

### <span data-ttu-id="46ff7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="46ff7-121">System.String</span></span>

## <span data-ttu-id="46ff7-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46ff7-122">OUTPUTS</span></span>

### <span data-ttu-id="46ff7-123">Microsoft. Azure. Commands. Maintenance. Models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="46ff7-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="46ff7-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="46ff7-124">NOTES</span></span>

## <span data-ttu-id="46ff7-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46ff7-125">RELATED LINKS</span></span>
