---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4dea211f2a09823161c1c6551b1fa00ab018a855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720481"
---
# <span data-ttu-id="581be-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="581be-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="581be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="581be-102">SYNOPSIS</span></span>
<span data-ttu-id="581be-103">Обновляет номер управляющей учетной записи, созданной с помощью элемента управления обменом (ICN), в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="581be-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="581be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="581be-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="581be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="581be-105">DESCRIPTION</span></span>
<span data-ttu-id="581be-106">Командлет Set-AzIntegrationAccountGeneratedIcn обновляет существующую учетную запись интеграции, созданную с помощью номера элемента управления обменом данными (ICN), и возвращает объект, представляющий номер элемента управления для учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="581be-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="581be-107">Используйте этот командлет, чтобы обновить номер элемента управления для учетной записи, созданной для интеграции.</span><span class="sxs-lookup"><span data-stu-id="581be-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="581be-108">Вы можете изменить номер управляющей учетной записи, созданной с помощью номера элемента управления, указав имя учетной записи интеграции, имя группы ресурсов и название соглашения.</span><span class="sxs-lookup"><span data-stu-id="581be-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="581be-109">С помощью этой команды вы не можете создать новую учетную запись интеграции с номером элемента управления обменом.</span><span class="sxs-lookup"><span data-stu-id="581be-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="581be-110">Чтобы использовать динамические параметры, просто введите их в команду или введите знак дефис (-), чтобы указать имя параметра, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="581be-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="581be-111">Если вы пропустили требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="581be-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="581be-112">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="581be-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="581be-113">Укажите параметр "-AgreementType", чтобы указать, нужно ли возвращаться возвращаемые числа X12 или EDIFACT</span><span class="sxs-lookup"><span data-stu-id="581be-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="581be-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="581be-114">EXAMPLES</span></span>

### <span data-ttu-id="581be-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="581be-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="581be-116">Эта команда возвращает для учетной записи интеграции, созданной X12, номер управляющего номера для определенного соглашения учетной записи интеграции, увеличивает его значение на 100, а затем производит обратное возвращение обновленного значения.</span><span class="sxs-lookup"><span data-stu-id="581be-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="581be-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="581be-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="581be-118">Эта команда возвращает для учетной записи интеграции, созданной EdifactIntegrationAccountAgreement, номер управляющего номера для определенного соглашения учетной записи интеграции, увеличивает его значение на 100, а затем производит обратное возвращение обновленного значения.</span><span class="sxs-lookup"><span data-stu-id="581be-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="581be-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="581be-119">PARAMETERS</span></span>

### <span data-ttu-id="581be-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="581be-120">-AgreementName</span></span>
<span data-ttu-id="581be-121">Имя соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="581be-121">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="581be-122">-AgreementType</span></span>
<span data-ttu-id="581be-123">Тип соглашения для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="581be-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="581be-124">-ControlNumber</span></span>
<span data-ttu-id="581be-125">Созданный управляющий номер новое значение.</span><span class="sxs-lookup"><span data-stu-id="581be-125">The generated control number new value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581be-126">-DefaultProfile</span></span>
<span data-ttu-id="581be-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="581be-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="581be-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="581be-128">-Name</span></span>
<span data-ttu-id="581be-129">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="581be-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="581be-130">-ResourceGroupName</span></span>
<span data-ttu-id="581be-131">Имя группы ресурсов для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="581be-131">The integration account resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581be-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="581be-132">-Confirm</span></span>
<span data-ttu-id="581be-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="581be-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="581be-134">-WhatIf</span></span>
<span data-ttu-id="581be-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="581be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="581be-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="581be-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581be-137">CommonParameters</span></span>
<span data-ttu-id="581be-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="581be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581be-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581be-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581be-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="581be-140">INPUTS</span></span>

### <span data-ttu-id="581be-141">System. String</span><span class="sxs-lookup"><span data-stu-id="581be-141">System.String</span></span>

## <span data-ttu-id="581be-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="581be-142">OUTPUTS</span></span>

### <span data-ttu-id="581be-143">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="581be-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="581be-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="581be-144">NOTES</span></span>

## <span data-ttu-id="581be-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="581be-145">RELATED LINKS</span></span>

[<span data-ttu-id="581be-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="581be-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

