---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413119"
---
# <span data-ttu-id="35ca4-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="35ca4-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="35ca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="35ca4-103">Этот cmdlet получает определенный полученный номер обмена для соглашения и значения номера для контроля.</span><span class="sxs-lookup"><span data-stu-id="35ca4-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="35ca4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35ca4-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35ca4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="35ca4-106">Этот cmdlet предназначен для проверки наличия полученного номера обмена данными в сценариях аварийного восстановления и (при желании) для удаления этой сущности с помощью Remove-AzIntegrationAccountReceivedIcn.</span><span class="sxs-lookup"><span data-stu-id="35ca4-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="35ca4-107">Укажите параметр "-AgreementType", чтобы указать, должны ли возвращаться номера управления X12 или Edifact</span><span class="sxs-lookup"><span data-stu-id="35ca4-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="35ca4-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35ca4-108">EXAMPLES</span></span>

### <span data-ttu-id="35ca4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35ca4-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="35ca4-110">Эта команда возвращает учетной записи интеграции X12 полученный номер управления для обмена по имени соглашения и значению номера.</span><span class="sxs-lookup"><span data-stu-id="35ca4-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="35ca4-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35ca4-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="35ca4-112">Эта команда возвращает учетной записи интеграции Edifact номер для обмена по имени соглашения и номеру контроля.</span><span class="sxs-lookup"><span data-stu-id="35ca4-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="35ca4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35ca4-113">PARAMETERS</span></span>

### <span data-ttu-id="35ca4-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="35ca4-114">-AgreementName</span></span>
<span data-ttu-id="35ca4-115">Имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="35ca4-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="35ca4-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="35ca4-116">-AgreementType</span></span>
<span data-ttu-id="35ca4-117">Тип соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="35ca4-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="35ca4-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="35ca4-118">-ControlNumberValue</span></span>
<span data-ttu-id="35ca4-119">Номер в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="35ca4-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="35ca4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ca4-120">-DefaultProfile</span></span>
<span data-ttu-id="35ca4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35ca4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35ca4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35ca4-122">-Name</span></span>
<span data-ttu-id="35ca4-123">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="35ca4-123">The integration account name.</span></span>

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

### <span data-ttu-id="35ca4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35ca4-124">-ResourceGroupName</span></span>
<span data-ttu-id="35ca4-125">Имя группы ресурсов учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="35ca4-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="35ca4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ca4-126">CommonParameters</span></span>
<span data-ttu-id="35ca4-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ca4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ca4-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ca4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ca4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35ca4-129">INPUTS</span></span>

### <span data-ttu-id="35ca4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="35ca4-130">System.String</span></span>

## <span data-ttu-id="35ca4-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35ca4-131">OUTPUTS</span></span>

### <span data-ttu-id="35ca4-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="35ca4-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="35ca4-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35ca4-133">NOTES</span></span>

## <span data-ttu-id="35ca4-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35ca4-134">RELATED LINKS</span></span>

[<span data-ttu-id="35ca4-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="35ca4-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="35ca4-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="35ca4-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
