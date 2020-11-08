---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075480"
---
# <span data-ttu-id="28253-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="28253-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="28253-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28253-102">SYNOPSIS</span></span>
<span data-ttu-id="28253-103">Запрос на перезагрузку или переобразировать одиночный экземпляр роли или все экземпляры роли определенной роли.</span><span class="sxs-lookup"><span data-stu-id="28253-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="28253-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28253-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="28253-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28253-105">DESCRIPTION</span></span>
<span data-ttu-id="28253-106">Командлет **Reset-AzureRoleInstance** запрашивает перезагрузку или переобразировать экземпляр роли, выполняющийся в развертывании.</span><span class="sxs-lookup"><span data-stu-id="28253-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="28253-107">Эта операция выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="28253-107">This operation executes synchronously.</span></span>
<span data-ttu-id="28253-108">При перезагрузке экземпляра роли Azure переводит экземпляр в автономный режим, перезапускает основную операционную систему для этого экземпляра и переводит экземпляр обратно в оперативный режим.</span><span class="sxs-lookup"><span data-stu-id="28253-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="28253-109">Любые данные, которые записываются на локальный диск, сохраняются во всех перезагрузках.</span><span class="sxs-lookup"><span data-stu-id="28253-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="28253-110">Все данные из памяти будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="28253-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="28253-111">Reimaging. в зависимости от типа роли, экземпляр роли получает различные действия.</span><span class="sxs-lookup"><span data-stu-id="28253-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="28253-112">Для веб-или рабочей роли, когда роль воспроизводится, Azure переводит роль в автономный режим и записывает новую установку гостевой операционной системы Azure на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="28253-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="28253-113">Затем роль снова будет переведена в режим онлайн.</span><span class="sxs-lookup"><span data-stu-id="28253-113">The role is then brought back online.</span></span>
<span data-ttu-id="28253-114">При повторном создании роли виртуальной машины Azure переводит ее в автономный режим, повторно применяет к ней настраиваемое изображение и переводит роль обратно в оперативный режим.</span><span class="sxs-lookup"><span data-stu-id="28253-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="28253-115">Azure пытается поддерживать данные в любых локальных ресурсах хранилища, когда роль передается. Однако в случае временного сбоя оборудования локальный ресурс хранилища может быть потерян.</span><span class="sxs-lookup"><span data-stu-id="28253-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="28253-116">Если ваше приложение запрашивает сохранение данных, рекомендуется использовать запись в устойчивый источник данных, например на диск Azure.</span><span class="sxs-lookup"><span data-stu-id="28253-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="28253-117">Любые данные, которые записываются в локальный каталог, отличный от того, который определен локальным ресурсом хранилища, будут потеряны при воссоздании роли.</span><span class="sxs-lookup"><span data-stu-id="28253-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="28253-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28253-118">EXAMPLES</span></span>

### <span data-ttu-id="28253-119">Пример 1: перезагрузка экземпляра роли</span><span class="sxs-lookup"><span data-stu-id="28253-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="28253-120">Эта команда перезагружает экземпляр роли с именем MyWebRole_IN_0 в промежуточном развертывании службы MySvc01.</span><span class="sxs-lookup"><span data-stu-id="28253-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="28253-121">Пример 2: переобразировать экземпляр роли</span><span class="sxs-lookup"><span data-stu-id="28253-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="28253-122">Эта команда переобразует экземпляры ролей в промежуточном развертывании облачной службы MySvc01.</span><span class="sxs-lookup"><span data-stu-id="28253-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="28253-123">Пример 3: переизображение всех экземпляров роли</span><span class="sxs-lookup"><span data-stu-id="28253-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="28253-124">Эта команда переобразует все экземпляры роли в рабочем развертывании службы MySvc01.</span><span class="sxs-lookup"><span data-stu-id="28253-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="28253-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28253-125">PARAMETERS</span></span>

### <span data-ttu-id="28253-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="28253-126">-InformationAction</span></span>
<span data-ttu-id="28253-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="28253-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="28253-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28253-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28253-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="28253-129">Continue</span></span>
- <span data-ttu-id="28253-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="28253-130">Ignore</span></span>
- <span data-ttu-id="28253-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="28253-131">Inquire</span></span>
- <span data-ttu-id="28253-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="28253-132">SilentlyContinue</span></span>
- <span data-ttu-id="28253-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="28253-133">Stop</span></span>
- <span data-ttu-id="28253-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="28253-134">Suspend</span></span>

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

### <span data-ttu-id="28253-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="28253-135">-InformationVariable</span></span>
<span data-ttu-id="28253-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="28253-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="28253-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="28253-137">-InstanceName</span></span>
<span data-ttu-id="28253-138">Указывает имя экземпляра роли для переустановки или перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="28253-138">Specifies the name of the role instance to reimage or reboot.</span></span>

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

### <span data-ttu-id="28253-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="28253-139">-Profile</span></span>
<span data-ttu-id="28253-140">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="28253-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28253-141">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28253-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28253-142">-Reboot</span><span class="sxs-lookup"><span data-stu-id="28253-142">-Reboot</span></span>
<span data-ttu-id="28253-143">Указывает, что этот командлет перезагружает указанный экземпляр роли или, если он не указан, для всех экземпляров роли.</span><span class="sxs-lookup"><span data-stu-id="28253-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="28253-144">Вы должны добавить параметр *reboot* или *Reimage* , но не оба.</span><span class="sxs-lookup"><span data-stu-id="28253-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28253-145">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="28253-145">-Reimage</span></span>
<span data-ttu-id="28253-146">Указывает на то, что этот командлет переобразировать указанный экземпляр роли или, если он не указан, для всех экземпляров роли.</span><span class="sxs-lookup"><span data-stu-id="28253-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="28253-147">Вы должны добавить параметр *reboot* или *Reimage* , но не оба.</span><span class="sxs-lookup"><span data-stu-id="28253-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28253-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="28253-148">-ServiceName</span></span>
<span data-ttu-id="28253-149">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="28253-149">Specifies the name of the service.</span></span>

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

### <span data-ttu-id="28253-150">-Slot</span><span class="sxs-lookup"><span data-stu-id="28253-150">-Slot</span></span>
<span data-ttu-id="28253-151">Указывает среду развертывания, в которой выполняются экземпляры роли.</span><span class="sxs-lookup"><span data-stu-id="28253-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="28253-152">Допустимые значения: "производство" и "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="28253-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="28253-153">Вы можете использовать параметр *DeploymentName* или *slot* , но не оба.</span><span class="sxs-lookup"><span data-stu-id="28253-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

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

### <span data-ttu-id="28253-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28253-154">CommonParameters</span></span>
<span data-ttu-id="28253-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28253-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28253-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28253-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28253-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28253-157">INPUTS</span></span>

## <span data-ttu-id="28253-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28253-158">OUTPUTS</span></span>

## <span data-ttu-id="28253-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="28253-159">NOTES</span></span>

## <span data-ttu-id="28253-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28253-160">RELATED LINKS</span></span>

[<span data-ttu-id="28253-161">Set-AzureRole</span><span class="sxs-lookup"><span data-stu-id="28253-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


