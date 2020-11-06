---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567834"
---
# <span data-ttu-id="76c85-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c85-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="76c85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76c85-102">SYNOPSIS</span></span>
<span data-ttu-id="76c85-103">Получает список конфигураций обновлений программного обеспечения службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="76c85-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76c85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76c85-104">SYNTAX</span></span>

### <span data-ttu-id="76c85-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76c85-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c85-106">ByName</span><span class="sxs-lookup"><span data-stu-id="76c85-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76c85-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="76c85-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76c85-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76c85-108">DESCRIPTION</span></span>
<span data-ttu-id="76c85-109">Get-AzureRmAutomationSoftwareUpdateConfiguration возвращает список конфигураций обновлений программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="76c85-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="76c85-110">Чтобы получить определенную конфигурацию обновления программного обеспечения, укажите параметр Name (имя).</span><span class="sxs-lookup"><span data-stu-id="76c85-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="76c85-111">Вы также можете вывести список конфигураций обновлений программного обеспечения, предназначенных для конкретной виртуальной машины Azure, указав идентификатор ресурса Azure для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="76c85-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="76c85-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76c85-112">EXAMPLES</span></span>

### <span data-ttu-id="76c85-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76c85-113">Example 1</span></span>
<span data-ttu-id="76c85-114">Получить конфигурацию обновления программного обеспечения Azure Automation по имени.</span><span class="sxs-lookup"><span data-stu-id="76c85-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="76c85-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76c85-115">PARAMETERS</span></span>

### <span data-ttu-id="76c85-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="76c85-116">-AutomationAccountName</span></span>
<span data-ttu-id="76c85-117">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="76c85-117">The automation account name.</span></span>

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

### <span data-ttu-id="76c85-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="76c85-118">-AzureVMResourceId</span></span>
<span data-ttu-id="76c85-119">Идентификатор ресурса Azure виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="76c85-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="76c85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c85-120">-DefaultProfile</span></span>
<span data-ttu-id="76c85-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76c85-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76c85-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76c85-122">-Name</span></span>
<span data-ttu-id="76c85-123">Название конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="76c85-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="76c85-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c85-124">-ResourceGroupName</span></span>
<span data-ttu-id="76c85-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76c85-125">The resource group name.</span></span>

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

### <span data-ttu-id="76c85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c85-126">CommonParameters</span></span>
<span data-ttu-id="76c85-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76c85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c85-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76c85-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c85-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76c85-129">INPUTS</span></span>

### <span data-ttu-id="76c85-130">System. String</span><span class="sxs-lookup"><span data-stu-id="76c85-130">System.String</span></span>

## <span data-ttu-id="76c85-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76c85-131">OUTPUTS</span></span>

### <span data-ttu-id="76c85-132">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="76c85-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="76c85-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="76c85-133">NOTES</span></span>

## <span data-ttu-id="76c85-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76c85-134">RELATED LINKS</span></span>
