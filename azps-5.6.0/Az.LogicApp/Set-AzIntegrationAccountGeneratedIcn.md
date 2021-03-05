---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4c91ced490226901a45e0eacb7caa204daa20558
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976808"
---
# <span data-ttu-id="321b8-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="321b8-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="321b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="321b8-102">SYNOPSIS</span></span>
<span data-ttu-id="321b8-103">Обновляет учетную запись интеграции, сгенерированную в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="321b8-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="321b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="321b8-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="321b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="321b8-105">DESCRIPTION</span></span>
<span data-ttu-id="321b8-106">С Set-AzIntegrationAccountGeneratedIcn- и других учетных записей обновляется номер, созданный для интеграции, и возвращается объект, который представляет собой сгенерированную учетную запись обмена.</span><span class="sxs-lookup"><span data-stu-id="321b8-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="321b8-107">Используйте этот cmdlet для обновления учетной записи интеграции, сгенерированной номером управления обмена данными.</span><span class="sxs-lookup"><span data-stu-id="321b8-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="321b8-108">Вы можете обновить сгенерированную учетную запись обмена, указав имя учетной записи интеграции, имя группы ресурсов и имя соглашения.</span><span class="sxs-lookup"><span data-stu-id="321b8-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="321b8-109">С помощью этой команды нельзя создать новую учетную запись интеграции, сгенерированную с помощью этого командного номера.</span><span class="sxs-lookup"><span data-stu-id="321b8-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="321b8-110">Чтобы использовать динамические параметры, просто введите их в команду или введите дефис (-), чтобы указать имя параметра, а затем несколько раз нажмите клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="321b8-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="321b8-111">Если вы пропустили необходимый параметр шаблона, будет предложено в этом случае.</span><span class="sxs-lookup"><span data-stu-id="321b8-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="321b8-112">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="321b8-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="321b8-113">Укажите параметр "-AgreementType", чтобы указать, должны ли возвращаться номера управления X12 или Edifact</span><span class="sxs-lookup"><span data-stu-id="321b8-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="321b8-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="321b8-114">EXAMPLES</span></span>

### <span data-ttu-id="321b8-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="321b8-115">Example 1</span></span>
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

<span data-ttu-id="321b8-116">Эта команда получает сгенерированную учетной записью интеграции номер управления X12 для определенного соглашения об учетной записи интеграции, увеличивает его значение на 100, а затем записывает обратно обновленное значение.</span><span class="sxs-lookup"><span data-stu-id="321b8-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="321b8-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="321b8-117">Example 2</span></span>
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

<span data-ttu-id="321b8-118">Эта команда получает учетную запись интеграции, созданную EdifactIntegrationAccountAgreement interchange control number для определенного соглашения об учетной записи интеграции, увеличивает его значение на 100, а затем записывает обратно обновленное значение.</span><span class="sxs-lookup"><span data-stu-id="321b8-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="321b8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="321b8-119">PARAMETERS</span></span>

### <span data-ttu-id="321b8-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="321b8-120">-AgreementName</span></span>
<span data-ttu-id="321b8-121">Имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="321b8-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="321b8-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="321b8-122">-AgreementType</span></span>
<span data-ttu-id="321b8-123">Тип соглашения об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="321b8-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="321b8-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="321b8-124">-ControlNumber</span></span>
<span data-ttu-id="321b8-125">Сгенерированная control number новое значение.</span><span class="sxs-lookup"><span data-stu-id="321b8-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="321b8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321b8-126">-DefaultProfile</span></span>
<span data-ttu-id="321b8-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="321b8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="321b8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="321b8-128">-Name</span></span>
<span data-ttu-id="321b8-129">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="321b8-129">The integration account name.</span></span>

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

### <span data-ttu-id="321b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="321b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="321b8-131">Имя группы ресурсов учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="321b8-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="321b8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="321b8-132">-Confirm</span></span>
<span data-ttu-id="321b8-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="321b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="321b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="321b8-134">-WhatIf</span></span>
<span data-ttu-id="321b8-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="321b8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="321b8-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="321b8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="321b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321b8-137">CommonParameters</span></span>
<span data-ttu-id="321b8-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="321b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321b8-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="321b8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321b8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="321b8-140">INPUTS</span></span>

### <span data-ttu-id="321b8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="321b8-141">System.String</span></span>

## <span data-ttu-id="321b8-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="321b8-142">OUTPUTS</span></span>

### <span data-ttu-id="321b8-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="321b8-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="321b8-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="321b8-144">NOTES</span></span>

## <span data-ttu-id="321b8-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="321b8-145">RELATED LINKS</span></span>

[<span data-ttu-id="321b8-146">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="321b8-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

