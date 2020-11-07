---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 3e4a8a68ce6af6a8be30750d0eaf8e5393ac409f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733708"
---
# <span data-ttu-id="b06ca-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b06ca-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="b06ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b06ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b06ca-103">Изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b06ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b06ca-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b06ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b06ca-105">DESCRIPTION</span></span>
<span data-ttu-id="b06ca-106">Командлет **Set-AzureRmIntegrationAccountMap** изменяет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="b06ca-107">Этот командлет возвращает объект, представляющий карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="b06ca-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="b06ca-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="b06ca-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="b06ca-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b06ca-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="b06ca-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b06ca-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="b06ca-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b06ca-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="b06ca-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b06ca-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b06ca-113">EXAMPLES</span></span>

### <span data-ttu-id="b06ca-114">Пример 1: изменение карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="b06ca-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="b06ca-115">Эта команда изменяет карту учетной записи интеграции в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b06ca-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="b06ca-116">Команда задает определение карты, которое хранится в переменной $MapContent с помощью предыдущей команды.</span><span class="sxs-lookup"><span data-stu-id="b06ca-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="b06ca-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b06ca-117">PARAMETERS</span></span>

### <span data-ttu-id="b06ca-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b06ca-118">-ContentType</span></span>
<span data-ttu-id="b06ca-119">Указывает тип контента для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="b06ca-120">Этот командлет поддерживает приложение и XML в качестве типа контента "карта".</span><span class="sxs-lookup"><span data-stu-id="b06ca-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="b06ca-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b06ca-121">-Force</span></span>
<span data-ttu-id="b06ca-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b06ca-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b06ca-123">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="b06ca-123">-MapDefinition</span></span>
<span data-ttu-id="b06ca-124">Указывает объект определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-124">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="b06ca-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="b06ca-125">-MapFilePath</span></span>
<span data-ttu-id="b06ca-126">Задает путь к файлу определения для карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-126">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="b06ca-127">-MapName</span><span class="sxs-lookup"><span data-stu-id="b06ca-127">-MapName</span></span>
<span data-ttu-id="b06ca-128">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-128">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="b06ca-129">-MapType</span><span class="sxs-lookup"><span data-stu-id="b06ca-129">-MapType</span></span>
<span data-ttu-id="b06ca-130">Указывает тип карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-130">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="b06ca-131">Этот командлет поддерживает преобразование XSLT в тип карты.</span><span class="sxs-lookup"><span data-stu-id="b06ca-131">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06ca-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b06ca-132">-Metadata</span></span>
<span data-ttu-id="b06ca-133">Указывает объект метаданных для карты.</span><span class="sxs-lookup"><span data-stu-id="b06ca-133">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="b06ca-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b06ca-134">-Name</span></span>
<span data-ttu-id="b06ca-135">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="b06ca-135">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b06ca-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b06ca-136">-ResourceGroupName</span></span>
<span data-ttu-id="b06ca-137">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b06ca-137">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b06ca-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b06ca-138">-Confirm</span></span>
<span data-ttu-id="b06ca-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b06ca-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b06ca-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b06ca-140">-WhatIf</span></span>
<span data-ttu-id="b06ca-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b06ca-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b06ca-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b06ca-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b06ca-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06ca-143">-DefaultProfile</span></span>
<span data-ttu-id="b06ca-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b06ca-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b06ca-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06ca-145">CommonParameters</span></span>
<span data-ttu-id="b06ca-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b06ca-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06ca-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b06ca-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06ca-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b06ca-148">INPUTS</span></span>

## <span data-ttu-id="b06ca-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b06ca-149">OUTPUTS</span></span>

### <span data-ttu-id="b06ca-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b06ca-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b06ca-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="b06ca-151">NOTES</span></span>

## <span data-ttu-id="b06ca-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b06ca-152">RELATED LINKS</span></span>

[<span data-ttu-id="b06ca-153">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b06ca-153">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b06ca-154">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b06ca-154">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b06ca-155">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b06ca-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


