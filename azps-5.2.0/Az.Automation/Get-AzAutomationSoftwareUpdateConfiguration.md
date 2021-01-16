---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418623"
---
# <span data-ttu-id="d4fa5-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa5-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d4fa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="d4fa5-103">Возвращает список конфигураций обновления программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="d4fa5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4fa5-104">SYNTAX</span></span>

### <span data-ttu-id="d4fa5-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4fa5-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4fa5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d4fa5-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4fa5-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="d4fa5-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4fa5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4fa5-108">DESCRIPTION</span></span>
<span data-ttu-id="d4fa5-109">В Get-AzAutomationSoftwareUpdateConfiguration возвращается список конфигураций обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="d4fa5-110">Чтобы получить определенную конфигурацию обновления программного обеспечения, укажите параметр имени.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="d4fa5-111">Вы также можете указать конфигурации обновления программного обеспечения, которые нацелены на конкретную виртуальную машину Azure, указав для нее ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="d4fa5-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4fa5-112">EXAMPLES</span></span>

### <span data-ttu-id="d4fa5-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4fa5-113">Example 1</span></span>
<span data-ttu-id="d4fa5-114">Получите конфигурацию обновления программного обеспечения автоматизации Azure по имени.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="d4fa5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4fa5-115">PARAMETERS</span></span>

### <span data-ttu-id="d4fa5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d4fa5-116">-AutomationAccountName</span></span>
<span data-ttu-id="d4fa5-117">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-117">The automation account name.</span></span>

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

### <span data-ttu-id="d4fa5-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="d4fa5-118">-AzureVMResourceId</span></span>
<span data-ttu-id="d4fa5-119">Azure resource Id of the virtual machine.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="d4fa5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fa5-120">-DefaultProfile</span></span>
<span data-ttu-id="d4fa5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4fa5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d4fa5-122">-Name</span></span>
<span data-ttu-id="d4fa5-123">Имя конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="d4fa5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4fa5-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4fa5-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-125">The resource group name.</span></span>

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

### <span data-ttu-id="d4fa5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fa5-126">CommonParameters</span></span>
<span data-ttu-id="d4fa5-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4fa5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fa5-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4fa5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4fa5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4fa5-129">INPUTS</span></span>

### <span data-ttu-id="d4fa5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d4fa5-130">System.String</span></span>

## <span data-ttu-id="d4fa5-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4fa5-131">OUTPUTS</span></span>

### <span data-ttu-id="d4fa5-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fa5-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d4fa5-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4fa5-133">NOTES</span></span>

## <span data-ttu-id="d4fa5-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4fa5-134">RELATED LINKS</span></span>