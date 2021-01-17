---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 146f1ba93a8df5f6a4396c30c9da451cdb89b9b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415564"
---
# <span data-ttu-id="6c94c-101">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="6c94c-101">Set-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="6c94c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c94c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c94c-103">Обновляет учетную запись интеграции с полученным номером управления обмена (ICN) в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6c94c-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="6c94c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6c94c-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c94c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c94c-105">DESCRIPTION</span></span>
<span data-ttu-id="6c94c-106">С Set-AzIntegrationAccountGeneratedIcn-код обновляет существующую учетную запись интеграции, полученный номер управления обмена (ICN), и возвращает объект, который представляет полученный номер управления для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c94c-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="6c94c-107">Используйте этот cmdlet для обновления состояния обработки сообщений для учетной записи интеграции, которая была получена через обмен данными.</span><span class="sxs-lookup"><span data-stu-id="6c94c-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="6c94c-108">Вы можете обновить полученный номер управления для интеграции, указав имя учетной записи интеграции, имя группы ресурсов, имя соглашения, номер управления номером и состояние обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c94c-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="6c94c-109">С помощью этой команды нельзя создать новую учетную запись интеграции с полученным номером управления обмена.</span><span class="sxs-lookup"><span data-stu-id="6c94c-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="6c94c-110">Чтобы использовать динамические параметры, просто введите их в команду или введите дефис (-), чтобы указать имя параметра, а затем несколько раз нажмите клавишу TAB для циклиального перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="6c94c-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6c94c-111">Если вы пропустили необходимый параметр шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="6c94c-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="6c94c-112">Значения файлов параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="6c94c-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6c94c-113">Укажите параметр "-AgreementType", чтобы указать, должны ли возвращаться номера управления X12 или Edifact</span><span class="sxs-lookup"><span data-stu-id="6c94c-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="6c94c-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6c94c-114">EXAMPLES</span></span>

### <span data-ttu-id="6c94c-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6c94c-115">Example 1</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="6c94c-116">Эта команда обновляет учетную запись интеграции, полученную с помощью X12 interchange control number для определенного соглашения об учетной записи интеграции, и значение со сбойом обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c94c-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="6c94c-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6c94c-117">Example 2</span></span>
```
PS C:\> Set-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="6c94c-118">Эта команда обновляет полученную учетную запись Edifact interchange control number для определенного соглашения об учетной записи интеграции и значение со сбойом обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6c94c-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="6c94c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c94c-119">PARAMETERS</span></span>

### <span data-ttu-id="6c94c-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6c94c-120">-AgreementName</span></span>
<span data-ttu-id="6c94c-121">Имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c94c-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="6c94c-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6c94c-122">-AgreementType</span></span>
<span data-ttu-id="6c94c-123">Тип соглашения об учетной записи интеграции (X12 или Edifact).</span><span class="sxs-lookup"><span data-stu-id="6c94c-123">The integration account agreement type (X12 or Edifact).</span></span>

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

### <span data-ttu-id="6c94c-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="6c94c-124">-ControlNumberValue</span></span>
<span data-ttu-id="6c94c-125">Номер в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c94c-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="6c94c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c94c-126">-DefaultProfile</span></span>
<span data-ttu-id="6c94c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6c94c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c94c-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="6c94c-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="6c94c-129">Состояние обработки полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="6c94c-129">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c94c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="6c94c-130">-Name</span></span>
<span data-ttu-id="6c94c-131">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c94c-131">The integration account name.</span></span>

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

### <span data-ttu-id="6c94c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c94c-132">-ResourceGroupName</span></span>
<span data-ttu-id="6c94c-133">Имя группы ресурсов учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="6c94c-133">The integration account resource group name.</span></span>

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

### <span data-ttu-id="6c94c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c94c-134">-Confirm</span></span>
<span data-ttu-id="6c94c-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6c94c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c94c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c94c-136">-WhatIf</span></span>
<span data-ttu-id="6c94c-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c94c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c94c-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6c94c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c94c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c94c-139">CommonParameters</span></span>
<span data-ttu-id="6c94c-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c94c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c94c-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c94c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c94c-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c94c-142">INPUTS</span></span>

### <span data-ttu-id="6c94c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6c94c-143">System.String</span></span>

## <span data-ttu-id="6c94c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6c94c-144">OUTPUTS</span></span>

### <span data-ttu-id="6c94c-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="6c94c-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="6c94c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6c94c-146">NOTES</span></span>

## <span data-ttu-id="6c94c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c94c-147">RELATED LINKS</span></span>

<span data-ttu-id="6c94c-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="6c94c-148">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Remove-AzIntegrationAccountReceivedIcn](./Remove-AzIntegrationAccountReceivedIcn.md)</span></span>
