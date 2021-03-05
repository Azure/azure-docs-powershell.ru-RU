---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: a87ccecbba21479c24a2defd2d7443f66184a799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961928"
---
# <span data-ttu-id="4eb72-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="4eb72-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="4eb72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb72-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb72-103">Этот cmdlet removes a specific received interchange control number per agreement and control number value.</span><span class="sxs-lookup"><span data-stu-id="4eb72-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="4eb72-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4eb72-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb72-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eb72-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb72-106">Этот cmdlet предназначен для использования в сценариях аварийного восстановления для удаления полученного номера управления обмена данными из учетной записи интеграции, чтобы соединитель B2B мог повторно обработать сообщение при включенной функции обнаружения повторяюх номеров.</span><span class="sxs-lookup"><span data-stu-id="4eb72-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="4eb72-107">В редких случаях полученный номер обмена обмена может быть зарезервирован незадолго до аварийного Скайп и до того, как соединитель B2B отклоняет этот обмен как ошибочный.</span><span class="sxs-lookup"><span data-stu-id="4eb72-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="4eb72-108">В таких случаях может потребоваться снова повторить обработку на сайте восстановления того же обмена данными после исправления его полезной нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4eb72-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="4eb72-109">Укажите параметр "-AgreementType", чтобы указать, должны ли возвращаться номера управления X12 или Edifact</span><span class="sxs-lookup"><span data-stu-id="4eb72-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="4eb72-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4eb72-110">EXAMPLES</span></span>

### <span data-ttu-id="4eb72-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4eb72-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="4eb72-112">Попытка получить полученный номер обмена данными X12, содержимое которого не имеет допустимого формата.</span><span class="sxs-lookup"><span data-stu-id="4eb72-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="4eb72-113">Удаляет полученный номер управления обмена X12.</span><span class="sxs-lookup"><span data-stu-id="4eb72-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="4eb72-114">Подтверждает, что полученный номер управления обмена данными X12 был удален при попытке получить его еще раз.</span><span class="sxs-lookup"><span data-stu-id="4eb72-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="4eb72-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4eb72-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="4eb72-116">Попытка получить полученный номер обмена данными Edifact, содержимое которого не имеет допустимого формата.</span><span class="sxs-lookup"><span data-stu-id="4eb72-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="4eb72-117">Удаляет полученный номер управления обмена Edifact.</span><span class="sxs-lookup"><span data-stu-id="4eb72-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="4eb72-118">Подтверждает, что полученный номер управления обмена данными Edifact удален путем попытки получить его еще раз.</span><span class="sxs-lookup"><span data-stu-id="4eb72-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="4eb72-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb72-119">PARAMETERS</span></span>

### <span data-ttu-id="4eb72-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="4eb72-120">-AgreementName</span></span>
<span data-ttu-id="4eb72-121">Имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4eb72-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="4eb72-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="4eb72-122">-AgreementType</span></span>
<span data-ttu-id="4eb72-123">Тип соглашения об интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="4eb72-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="4eb72-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="4eb72-124">-ControlNumberValue</span></span>
<span data-ttu-id="4eb72-125">Номер в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4eb72-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="4eb72-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb72-126">-DefaultProfile</span></span>
<span data-ttu-id="4eb72-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4eb72-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb72-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb72-128">-Name</span></span>
<span data-ttu-id="4eb72-129">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4eb72-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb72-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb72-130">-ResourceGroupName</span></span>
<span data-ttu-id="4eb72-131">Имя группы ресурсов учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="4eb72-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="4eb72-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4eb72-132">-Confirm</span></span>
<span data-ttu-id="4eb72-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb72-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb72-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb72-134">-WhatIf</span></span>
<span data-ttu-id="4eb72-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb72-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb72-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4eb72-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb72-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb72-137">CommonParameters</span></span>
<span data-ttu-id="4eb72-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb72-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb72-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb72-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb72-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb72-140">INPUTS</span></span>

### <span data-ttu-id="4eb72-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4eb72-141">System.String</span></span>

## <span data-ttu-id="4eb72-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb72-142">OUTPUTS</span></span>

### <span data-ttu-id="4eb72-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="4eb72-143">System.Void</span></span>

## <span data-ttu-id="4eb72-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4eb72-144">NOTES</span></span>

## <span data-ttu-id="4eb72-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4eb72-145">RELATED LINKS</span></span>

<span data-ttu-id="4eb72-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
 [Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="4eb72-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

