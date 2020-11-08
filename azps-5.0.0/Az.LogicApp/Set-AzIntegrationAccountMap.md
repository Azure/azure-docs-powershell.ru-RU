---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250125"
---
# <span data-ttu-id="f6420-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f6420-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="f6420-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6420-102">SYNOPSIS</span></span>
<span data-ttu-id="f6420-103">Изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="f6420-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6420-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6420-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6420-105">DESCRIPTION</span></span>
<span data-ttu-id="f6420-106">Командлет **Set-AzIntegrationAccountMap** изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="f6420-107">Этот командлет возвращает объект, представляющий карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="f6420-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="f6420-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="f6420-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f6420-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f6420-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f6420-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f6420-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f6420-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f6420-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f6420-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f6420-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6420-113">EXAMPLES</span></span>

### <span data-ttu-id="f6420-114">Пример 1: изменение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="f6420-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="f6420-115">Эта команда изменяет карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6420-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="f6420-116">Команда задает определение карты, которое хранится в переменной $MapContent с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="f6420-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="f6420-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f6420-117">Example 2</span></span>

<span data-ttu-id="f6420-118">Изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-118">Modifies an integration account map.</span></span> <span data-ttu-id="f6420-119">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="f6420-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="f6420-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6420-120">PARAMETERS</span></span>

### <span data-ttu-id="f6420-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="f6420-121">-ContentType</span></span>
<span data-ttu-id="f6420-122">Указывает тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="f6420-123">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="f6420-123">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6420-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6420-124">-DefaultProfile</span></span>
<span data-ttu-id="f6420-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6420-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6420-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f6420-126">-Force</span></span>
<span data-ttu-id="f6420-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f6420-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6420-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="f6420-128">-MapDefinition</span></span>
<span data-ttu-id="f6420-129">Указывает объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-129">Specifies a definition object for integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6420-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="f6420-130">-MapFilePath</span></span>
<span data-ttu-id="f6420-131">Задает путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-131">Specifies the file path of a definition for the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6420-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="f6420-132">-MapName</span></span>
<span data-ttu-id="f6420-133">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="f6420-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="f6420-134">-MapType</span></span>
<span data-ttu-id="f6420-135">Указывает тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="f6420-136">Этот командлет поддерживает преобразование XSLT в тип карты.</span><span class="sxs-lookup"><span data-stu-id="f6420-136">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6420-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f6420-137">-Metadata</span></span>
<span data-ttu-id="f6420-138">Указывает объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="f6420-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="f6420-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6420-139">-Name</span></span>
<span data-ttu-id="f6420-140">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f6420-140">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6420-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6420-141">-ResourceGroupName</span></span>
<span data-ttu-id="f6420-142">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6420-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f6420-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6420-143">-Confirm</span></span>
<span data-ttu-id="f6420-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6420-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6420-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6420-145">-WhatIf</span></span>
<span data-ttu-id="f6420-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6420-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6420-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6420-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6420-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6420-148">CommonParameters</span></span>
<span data-ttu-id="f6420-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6420-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6420-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6420-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6420-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6420-151">INPUTS</span></span>

### <span data-ttu-id="f6420-152">System. String</span><span class="sxs-lookup"><span data-stu-id="f6420-152">System.String</span></span>

## <span data-ttu-id="f6420-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6420-153">OUTPUTS</span></span>

### <span data-ttu-id="f6420-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f6420-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="f6420-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6420-155">NOTES</span></span>

## <span data-ttu-id="f6420-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6420-156">RELATED LINKS</span></span>

[<span data-ttu-id="f6420-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f6420-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="f6420-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f6420-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="f6420-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f6420-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


