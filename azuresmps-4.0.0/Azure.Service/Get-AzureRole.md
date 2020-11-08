---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076314"
---
# <span data-ttu-id="a7bc2-101">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="a7bc2-101">Get-AzureRole</span></span>

## <span data-ttu-id="a7bc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bc2-103">Возвращает список ролей в службе Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-103">Returns a list of roles in your Microsoft Azure service.</span></span>

## <span data-ttu-id="a7bc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7bc2-104">SYNTAX</span></span>

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7bc2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7bc2-105">DESCRIPTION</span></span>
<span data-ttu-id="a7bc2-106">Командлет **Get-AzureRole** возвращает объект списка с подробными сведениями о ролях в службе Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-106">The **Get-AzureRole** cmdlet returns a list object with details on the roles in your Microsoft Azure service.</span></span>
<span data-ttu-id="a7bc2-107">Если указан параметр *roleName* , **Get-AzureRole** возвращает сведения только для этой роли.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-107">If you specify the *RoleName* parameter, **Get-AzureRole** returns details on that role only.</span></span>
<span data-ttu-id="a7bc2-108">Если указан параметр *InstanceDetails* , возвращаются дополнительные сведения, относящиеся к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-108">If you specify the *InstanceDetails* parameter, additional, instance-specific details are returned.</span></span>

## <span data-ttu-id="a7bc2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7bc2-109">EXAMPLES</span></span>

### <span data-ttu-id="a7bc2-110">Пример 1: получение списка ролей для службы</span><span class="sxs-lookup"><span data-stu-id="a7bc2-110">Example 1: Get a list of roles for a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

<span data-ttu-id="a7bc2-111">Эта команда возвращает объект с подробными сведениями о всех производственных ролях, запущенных в службе MySvc01.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-111">This command returns an object with details on all the production roles running on the MySvc01 service.</span></span>

### <span data-ttu-id="a7bc2-112">Пример 2: получение подробных сведений о роли, работающей в службе</span><span class="sxs-lookup"><span data-stu-id="a7bc2-112">Example 2: Get details on a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

<span data-ttu-id="a7bc2-113">Эта команда возвращает объект с подробными сведениями о роли MyTestVM3, который выполняется в промежуточной среде службы MySvc01.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-113">This command returns an object with details on the MyTestVM3 role, running on the staging environment of the MySvc01 service.</span></span>

### <span data-ttu-id="a7bc2-114">Пример 3: получение сведений об экземпляре роли, запущенной в службе</span><span class="sxs-lookup"><span data-stu-id="a7bc2-114">Example 3: Get instance information on instances of a role running on a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

<span data-ttu-id="a7bc2-115">Эта команда возвращает объект с подробными сведениями о экземплярах роли MyTestVM02, запущенных в рабочей среде службы MySvc01.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-115">This command returns an object with details on the instances of the MyTestVM02 role running in the production environment on the MySvc01 service.</span></span>

### <span data-ttu-id="a7bc2-116">Пример 4: получение таблицы с экземплярами ролей, связанными со службой</span><span class="sxs-lookup"><span data-stu-id="a7bc2-116">Example 4: Get a table of the role instances associated with a service</span></span>
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

<span data-ttu-id="a7bc2-117">Эта команда возвращает таблицу с именем экземпляра, размером и состоянием всех экземпляров роли, запущенных в рабочей среде в службе MySvc01.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-117">This command returns a table of the instance name, size, and status of all role instances running in the production environment on the MySvc01 service.</span></span>

## <span data-ttu-id="a7bc2-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7bc2-118">PARAMETERS</span></span>

### <span data-ttu-id="a7bc2-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a7bc2-119">-InformationAction</span></span>
<span data-ttu-id="a7bc2-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a7bc2-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a7bc2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7bc2-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a7bc2-122">Continue</span></span>
- <span data-ttu-id="a7bc2-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a7bc2-123">Ignore</span></span>
- <span data-ttu-id="a7bc2-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a7bc2-124">Inquire</span></span>
- <span data-ttu-id="a7bc2-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a7bc2-125">SilentlyContinue</span></span>
- <span data-ttu-id="a7bc2-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="a7bc2-126">Stop</span></span>
- <span data-ttu-id="a7bc2-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="a7bc2-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a7bc2-128">-InformationVariable</span></span>
<span data-ttu-id="a7bc2-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-130">-InstanceDetails</span><span class="sxs-lookup"><span data-stu-id="a7bc2-130">-InstanceDetails</span></span>
<span data-ttu-id="a7bc2-131">Указывает, что этот командлет возвращает сведения о экземплярах каждой роли.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-131">Specifies that this cmdlet returns details about the instances on each role.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="a7bc2-132">-Profile</span></span>
<span data-ttu-id="a7bc2-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7bc2-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-135">-RoleName</span><span class="sxs-lookup"><span data-stu-id="a7bc2-135">-RoleName</span></span>
<span data-ttu-id="a7bc2-136">Указывает имя роли для получения.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-136">Specifies the name of the role to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a7bc2-137">-ServiceName</span></span>
<span data-ttu-id="a7bc2-138">Указывает имя службы Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-138">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="a7bc2-139">-Slot</span></span>
<span data-ttu-id="a7bc2-140">Указывает среду развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-140">Specifies the Azure deployment environment.</span></span>
<span data-ttu-id="a7bc2-141">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="a7bc2-141">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7bc2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bc2-142">CommonParameters</span></span>
<span data-ttu-id="a7bc2-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7bc2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bc2-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7bc2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bc2-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7bc2-145">INPUTS</span></span>

## <span data-ttu-id="a7bc2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7bc2-146">OUTPUTS</span></span>

## <span data-ttu-id="a7bc2-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7bc2-147">NOTES</span></span>

## <span data-ttu-id="a7bc2-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7bc2-148">RELATED LINKS</span></span>

[<span data-ttu-id="a7bc2-149">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="a7bc2-149">Set-AzureRole</span></span>](./Set-AzureRole.md)


