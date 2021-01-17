---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395215"
---
# <span data-ttu-id="c38b8-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c38b8-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="c38b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c38b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c38b8-103">Задает значения свойств для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="c38b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c38b8-104">SYNTAX</span></span>

### <span data-ttu-id="c38b8-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38b8-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c38b8-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="c38b8-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c38b8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c38b8-107">DESCRIPTION</span></span>
<span data-ttu-id="c38b8-108">**Многлет Set-AzNotificationHub** изменяет значения свойств концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="c38b8-109">Значение свойства концентратора уведомлений можно изменить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="c38b8-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="c38b8-110">Например, вы можете создать экземпляр объекта **NotificationHubAttributes,** а затем настроить его со значениями свойств, которые вы хотите использовать для нового концентратора.</span><span class="sxs-lookup"><span data-stu-id="c38b8-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="c38b8-111">Это можно сделать через .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c38b8-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="c38b8-112">Затем вы можете скопировать значения этих свойств в свой центр с помощью *параметра NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="c38b8-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="c38b8-113">Кроме того, можно создать файл нотации объектов JSON (JavaScript), содержащий соответствующие значения конфигурации, а затем применить их с помощью параметра *InputFile.*</span><span class="sxs-lookup"><span data-stu-id="c38b8-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="c38b8-114">JSON-файл — это текстовый файл с синтаксисом, аналогичным следующему: {</span><span class="sxs-lookup"><span data-stu-id="c38b8-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="c38b8-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="c38b8-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="c38b8-116">"Location": "West US",</span><span class="sxs-lookup"><span data-stu-id="c38b8-116">"Location": "West US",</span></span>  
<span data-ttu-id="c38b8-117">} При использовании в сочетании с **cmdlet Set-AzNotificationHub** в предыдущем примере JSON задается значение расположения концентратора уведомлений ContosoNotificationHub на запад США.</span><span class="sxs-lookup"><span data-stu-id="c38b8-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="c38b8-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c38b8-118">EXAMPLES</span></span>

### <span data-ttu-id="c38b8-119">Пример 1. Изменение значений свойств для концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="c38b8-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="c38b8-120">Эта команда изменяет значения свойств концентратора уведомлений, найденного в области имен ContosoNamespace, и назначена группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="c38b8-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="c38b8-121">Значения свойств, а также имя центра, который нужно изменить, не указаны в команде.</span><span class="sxs-lookup"><span data-stu-id="c38b8-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="c38b8-122">Эти сведения будут содержаться во входных файлах, C:\Configuration\Hubs.jsних.</span><span class="sxs-lookup"><span data-stu-id="c38b8-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="c38b8-123">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c38b8-123">Example 2</span></span>

<span data-ttu-id="c38b8-124">Задает значения свойств для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="c38b8-125">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c38b8-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="c38b8-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c38b8-126">PARAMETERS</span></span>

### <span data-ttu-id="c38b8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38b8-127">-DefaultProfile</span></span>
<span data-ttu-id="c38b8-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c38b8-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c38b8-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c38b8-129">-Force</span></span>
<span data-ttu-id="c38b8-130">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c38b8-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c38b8-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="c38b8-131">-InputFile</span></span>
<span data-ttu-id="c38b8-132">Путь к JSON-файлу, который содержит сведения о конфигурации для концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b8-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c38b8-133">-Namespace</span></span>
<span data-ttu-id="c38b8-134">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="c38b8-135">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38b8-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="c38b8-136">-NotificationHubObj</span></span>
<span data-ttu-id="c38b8-137">Указывает объект **NotificationHubAttributes,** который содержит сведения о конфигурации для концентратора, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38b8-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b8-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c38b8-138">-ResourceGroup</span></span>
<span data-ttu-id="c38b8-139">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c38b8-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="c38b8-140">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="c38b8-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38b8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c38b8-141">-Confirm</span></span>
<span data-ttu-id="c38b8-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38b8-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38b8-143">-WhatIf</span></span>
<span data-ttu-id="c38b8-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38b8-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c38b8-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c38b8-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38b8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38b8-146">CommonParameters</span></span>
<span data-ttu-id="c38b8-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38b8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38b8-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c38b8-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38b8-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c38b8-149">INPUTS</span></span>

### <span data-ttu-id="c38b8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c38b8-150">System.String</span></span>

## <span data-ttu-id="c38b8-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c38b8-151">OUTPUTS</span></span>

### <span data-ttu-id="c38b8-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c38b8-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="c38b8-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c38b8-153">NOTES</span></span>

## <span data-ttu-id="c38b8-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c38b8-154">RELATED LINKS</span></span>

[<span data-ttu-id="c38b8-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c38b8-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="c38b8-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c38b8-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="c38b8-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="c38b8-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)


