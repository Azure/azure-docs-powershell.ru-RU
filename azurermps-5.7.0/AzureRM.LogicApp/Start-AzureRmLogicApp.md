---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734993"
---
# <span data-ttu-id="7d594-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7d594-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="7d594-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d594-102">SYNOPSIS</span></span>
<span data-ttu-id="7d594-103">Запускает логическое приложение в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d594-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d594-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d594-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d594-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d594-105">DESCRIPTION</span></span>
<span data-ttu-id="7d594-106">Командлет **Start-AzureRmLogicApp** запускает логическое приложение с помощью функции "приложения логики".</span><span class="sxs-lookup"><span data-stu-id="7d594-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="7d594-107">Укажите имя, группу ресурсов и триггер.</span><span class="sxs-lookup"><span data-stu-id="7d594-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="7d594-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="7d594-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7d594-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="7d594-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7d594-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="7d594-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7d594-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="7d594-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7d594-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d594-112">EXAMPLES</span></span>

### <span data-ttu-id="7d594-113">Пример 1: запуск приложения логики</span><span class="sxs-lookup"><span data-stu-id="7d594-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="7d594-114">Эта команда запускает приложение Logic в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7d594-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="7d594-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d594-115">PARAMETERS</span></span>

### <span data-ttu-id="7d594-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d594-116">-DefaultProfile</span></span>
<span data-ttu-id="7d594-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d594-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d594-118">-Name</span></span>
<span data-ttu-id="7d594-119">Указывает имя приложения логики, с которого начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7d594-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="7d594-120">-Parameters</span></span>
<span data-ttu-id="7d594-121">Указывает объект коллекции Parameters для приложения логики.</span><span class="sxs-lookup"><span data-stu-id="7d594-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="7d594-122">Укажите хэш-таблицу, словарь \<string\> или словарь \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="7d594-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d594-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d594-124">Указывает имя группы ресурсов, которая содержит логическое приложение, которое запускает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7d594-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="7d594-125">-TriggerName</span></span>
<span data-ttu-id="7d594-126">Задает имя триггера приложения логики, с которого начинается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7d594-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d594-127">-Confirm</span></span>
<span data-ttu-id="7d594-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d594-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d594-129">-WhatIf</span></span>
<span data-ttu-id="7d594-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d594-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d594-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d594-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d594-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d594-132">CommonParameters</span></span>
<span data-ttu-id="7d594-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d594-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d594-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d594-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d594-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d594-135">INPUTS</span></span>

### <span data-ttu-id="7d594-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="7d594-136">None</span></span>
<span data-ttu-id="7d594-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7d594-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d594-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d594-138">OUTPUTS</span></span>

### <span data-ttu-id="7d594-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="7d594-139">System.Object</span></span>

## <span data-ttu-id="7d594-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d594-140">NOTES</span></span>

## <span data-ttu-id="7d594-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d594-141">RELATED LINKS</span></span>

[<span data-ttu-id="7d594-142">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7d594-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="7d594-143">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="7d594-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="7d594-144">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7d594-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="7d594-145">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7d594-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="7d594-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7d594-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="7d594-147">Остановить-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="7d594-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


