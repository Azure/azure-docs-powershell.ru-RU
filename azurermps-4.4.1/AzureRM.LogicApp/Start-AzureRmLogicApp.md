---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: ed8a8c198f626d569d47a9b06b6d9595517f2f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570375"
---
# <span data-ttu-id="2fdf5-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fdf5-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="2fdf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fdf5-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdf5-103">Запускает логическое приложение в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fdf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fdf5-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fdf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fdf5-105">DESCRIPTION</span></span>
<span data-ttu-id="2fdf5-106">Командлет **Start-AzureRmLogicApp** запускает логическое приложение с помощью функции "приложения логики".</span><span class="sxs-lookup"><span data-stu-id="2fdf5-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="2fdf5-107">Укажите имя, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="2fdf5-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2fdf5-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2fdf5-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2fdf5-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2fdf5-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fdf5-112">EXAMPLES</span></span>

### <span data-ttu-id="2fdf5-113">Пример 1: запуск приложения логики</span><span class="sxs-lookup"><span data-stu-id="2fdf5-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="2fdf5-114">Эта команда запускает приложение Logic в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2fdf5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fdf5-115">PARAMETERS</span></span>

### <span data-ttu-id="2fdf5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fdf5-116">-Name</span></span>
<span data-ttu-id="2fdf5-117">Указывает имя приложения логики, с которого начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-117">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fdf5-118">-Parameters</span><span class="sxs-lookup"><span data-stu-id="2fdf5-118">-Parameters</span></span>
<span data-ttu-id="2fdf5-119">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-119">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="2fdf5-120">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="2fdf5-120">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdf5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdf5-121">-ResourceGroupName</span></span>
<span data-ttu-id="2fdf5-122">Указывает имя группы ресурсов, которая содержит логическое приложение, которое запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-122">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="2fdf5-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="2fdf5-123">-TriggerName</span></span>
<span data-ttu-id="2fdf5-124">Задает имя триггера приложения логики, с которого начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-124">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="2fdf5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fdf5-125">-Confirm</span></span>
<span data-ttu-id="2fdf5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdf5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdf5-127">-WhatIf</span></span>
<span data-ttu-id="2fdf5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fdf5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdf5-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdf5-130">-DefaultProfile</span></span>
<span data-ttu-id="2fdf5-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fdf5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdf5-132">CommonParameters</span></span>
<span data-ttu-id="2fdf5-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fdf5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdf5-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdf5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdf5-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fdf5-135">INPUTS</span></span>

## <span data-ttu-id="2fdf5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fdf5-136">OUTPUTS</span></span>

### <span data-ttu-id="2fdf5-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="2fdf5-137">System.Object</span></span>

## <span data-ttu-id="2fdf5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fdf5-138">NOTES</span></span>

## <span data-ttu-id="2fdf5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fdf5-139">RELATED LINKS</span></span>

[<span data-ttu-id="2fdf5-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fdf5-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="2fdf5-141">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="2fdf5-141">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="2fdf5-142">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fdf5-142">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="2fdf5-143">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fdf5-143">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="2fdf5-144">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fdf5-144">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="2fdf5-145">Остановить-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="2fdf5-145">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


