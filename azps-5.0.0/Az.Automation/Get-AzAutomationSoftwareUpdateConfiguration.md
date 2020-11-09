---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319358"
---
# <span data-ttu-id="3ce17-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ce17-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3ce17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ce17-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce17-103">Получает список конфигураций обновлений программного обеспечения службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce17-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="3ce17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ce17-104">SYNTAX</span></span>

### <span data-ttu-id="3ce17-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ce17-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce17-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3ce17-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce17-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="3ce17-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce17-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce17-108">DESCRIPTION</span></span>
<span data-ttu-id="3ce17-109">Get-AzAutomationSoftwareUpdateConfiguration возвращает список конфигураций обновлений программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3ce17-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="3ce17-110">Чтобы получить определенную конфигурацию обновления программного обеспечения, укажите параметр Name (имя).</span><span class="sxs-lookup"><span data-stu-id="3ce17-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="3ce17-111">Вы также можете вывести список конфигураций обновлений программного обеспечения, предназначенных для конкретной виртуальной машины Azure, указав идентификатор ресурса Azure для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3ce17-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="3ce17-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ce17-112">EXAMPLES</span></span>

### <span data-ttu-id="3ce17-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ce17-113">Example 1</span></span>
<span data-ttu-id="3ce17-114">Получить конфигурацию обновления программного обеспечения Azure Automation по имени.</span><span class="sxs-lookup"><span data-stu-id="3ce17-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="3ce17-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ce17-115">PARAMETERS</span></span>

### <span data-ttu-id="3ce17-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ce17-116">-AutomationAccountName</span></span>
<span data-ttu-id="3ce17-117">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3ce17-117">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce17-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="3ce17-118">-AzureVMResourceId</span></span>
<span data-ttu-id="3ce17-119">Идентификатор ресурса Azure виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3ce17-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce17-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce17-120">-DefaultProfile</span></span>
<span data-ttu-id="3ce17-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ce17-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce17-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ce17-122">-Name</span></span>
<span data-ttu-id="3ce17-123">Название конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3ce17-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce17-124">-ResourceGroupName</span></span>
<span data-ttu-id="3ce17-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ce17-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce17-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce17-126">CommonParameters</span></span>
<span data-ttu-id="3ce17-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ce17-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce17-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce17-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce17-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ce17-129">INPUTS</span></span>

### <span data-ttu-id="3ce17-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce17-130">System.String</span></span>

## <span data-ttu-id="3ce17-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce17-131">OUTPUTS</span></span>

### <span data-ttu-id="3ce17-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ce17-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3ce17-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ce17-133">NOTES</span></span>

## <span data-ttu-id="3ce17-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ce17-134">RELATED LINKS</span></span>