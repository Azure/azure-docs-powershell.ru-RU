---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: f963a89e6220e8154c2ba958adca318036c53474
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972739"
---
# <span data-ttu-id="310bf-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="310bf-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="310bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="310bf-102">SYNOPSIS</span></span>
<span data-ttu-id="310bf-103">Изменяет интеграцию с картой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="310bf-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="310bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="310bf-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="310bf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="310bf-105">DESCRIPTION</span></span>
<span data-ttu-id="310bf-106">**CmdletMap Set-AzIntegrationAccountMap** изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="310bf-107">Этот cmdlet возвращает объект, который представляет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="310bf-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="310bf-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="310bf-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="310bf-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="310bf-110">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="310bf-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="310bf-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="310bf-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="310bf-112">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="310bf-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="310bf-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="310bf-113">EXAMPLES</span></span>

### <span data-ttu-id="310bf-114">Пример 1. Изменение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="310bf-114">Example 1: Modify an integration account map</span></span>
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

<span data-ttu-id="310bf-115">Эта команда изменяет карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="310bf-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="310bf-116">Эта команда определяет определение карты, храняное в переменной $MapContent предыдущей командой.</span><span class="sxs-lookup"><span data-stu-id="310bf-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="310bf-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="310bf-117">Example 2</span></span>

<span data-ttu-id="310bf-118">Изменяет интеграцию с картой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="310bf-118">Modifies an integration account map.</span></span> <span data-ttu-id="310bf-119">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="310bf-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="310bf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="310bf-120">PARAMETERS</span></span>

### <span data-ttu-id="310bf-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="310bf-121">-ContentType</span></span>
<span data-ttu-id="310bf-122">Тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="310bf-123">Этот cmdlet поддерживает приложения и XML как тип контента карты.</span><span class="sxs-lookup"><span data-stu-id="310bf-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="310bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310bf-124">-DefaultProfile</span></span>
<span data-ttu-id="310bf-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="310bf-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="310bf-126">-Force</span><span class="sxs-lookup"><span data-stu-id="310bf-126">-Force</span></span>
<span data-ttu-id="310bf-127">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="310bf-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="310bf-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="310bf-128">-MapDefinition</span></span>
<span data-ttu-id="310bf-129">Определяет объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="310bf-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="310bf-130">-MapFilePath</span></span>
<span data-ttu-id="310bf-131">Путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="310bf-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="310bf-132">-MapName</span></span>
<span data-ttu-id="310bf-133">Указывает имя интеграционной карты учетной записи.</span><span class="sxs-lookup"><span data-stu-id="310bf-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="310bf-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="310bf-134">-MapType</span></span>
<span data-ttu-id="310bf-135">Тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="310bf-136">Этот cmdlet поддерживает XSLT как тип карты.</span><span class="sxs-lookup"><span data-stu-id="310bf-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="310bf-137">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="310bf-137">-Metadata</span></span>
<span data-ttu-id="310bf-138">Определяет объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="310bf-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="310bf-139">-Name</span><span class="sxs-lookup"><span data-stu-id="310bf-139">-Name</span></span>
<span data-ttu-id="310bf-140">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="310bf-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="310bf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="310bf-141">-ResourceGroupName</span></span>
<span data-ttu-id="310bf-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="310bf-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="310bf-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="310bf-143">-Confirm</span></span>
<span data-ttu-id="310bf-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="310bf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="310bf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="310bf-145">-WhatIf</span></span>
<span data-ttu-id="310bf-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="310bf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="310bf-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="310bf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="310bf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310bf-148">CommonParameters</span></span>
<span data-ttu-id="310bf-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="310bf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310bf-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="310bf-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310bf-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="310bf-151">INPUTS</span></span>

### <span data-ttu-id="310bf-152">System.String</span><span class="sxs-lookup"><span data-stu-id="310bf-152">System.String</span></span>

## <span data-ttu-id="310bf-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="310bf-153">OUTPUTS</span></span>

### <span data-ttu-id="310bf-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="310bf-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="310bf-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="310bf-155">NOTES</span></span>

## <span data-ttu-id="310bf-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="310bf-156">RELATED LINKS</span></span>

[<span data-ttu-id="310bf-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="310bf-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="310bf-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="310bf-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="310bf-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="310bf-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


