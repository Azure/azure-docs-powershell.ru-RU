---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076165"
---
# <span data-ttu-id="e56c9-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e56c9-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="e56c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e56c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e56c9-103">Удаляет Развертывание облачной службы.</span><span class="sxs-lookup"><span data-stu-id="e56c9-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="e56c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e56c9-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e56c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e56c9-105">DESCRIPTION</span></span>
<span data-ttu-id="e56c9-106">Командлет **Remove-AzureDeployment** удаляет Развертывание облачной службы Azure.</span><span class="sxs-lookup"><span data-stu-id="e56c9-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="e56c9-107">Чтобы удалить развертывание, сначала приостановите его.</span><span class="sxs-lookup"><span data-stu-id="e56c9-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="e56c9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e56c9-108">EXAMPLES</span></span>

### <span data-ttu-id="e56c9-109">Пример 1: Удаление развертывания</span><span class="sxs-lookup"><span data-stu-id="e56c9-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="e56c9-110">Эта команда удаляет развертывание службы Azure с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="e56c9-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="e56c9-111">Так как эта команда не задает слот, она удаляет службу из рабочей среды.</span><span class="sxs-lookup"><span data-stu-id="e56c9-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="e56c9-112">Пример 2: Удаление развертывания и виртуальных жестких дисков</span><span class="sxs-lookup"><span data-stu-id="e56c9-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="e56c9-113">Эта команда удаляет из рабочей среды развертывание службы с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="e56c9-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="e56c9-114">Команда также удаляет базовые виртуальные жесткие диски.</span><span class="sxs-lookup"><span data-stu-id="e56c9-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="e56c9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e56c9-115">PARAMETERS</span></span>

### <span data-ttu-id="e56c9-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="e56c9-116">-DeleteVHD</span></span>
<span data-ttu-id="e56c9-117">Указывает, что этот командлет удаляет развертывание и виртуальные жесткие диски (VHD) из хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="e56c9-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56c9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e56c9-118">-Force</span></span>
<span data-ttu-id="e56c9-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e56c9-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e56c9-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e56c9-120">-InformationAction</span></span>
<span data-ttu-id="e56c9-121">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="e56c9-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e56c9-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e56c9-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e56c9-123">Продолжал</span><span class="sxs-lookup"><span data-stu-id="e56c9-123">Continue</span></span>
- <span data-ttu-id="e56c9-124">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="e56c9-124">Ignore</span></span>
- <span data-ttu-id="e56c9-125">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="e56c9-125">Inquire</span></span>
- <span data-ttu-id="e56c9-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e56c9-126">SilentlyContinue</span></span>
- <span data-ttu-id="e56c9-127">Остановить</span><span class="sxs-lookup"><span data-stu-id="e56c9-127">Stop</span></span>
- <span data-ttu-id="e56c9-128">Рвать</span><span class="sxs-lookup"><span data-stu-id="e56c9-128">Suspend</span></span>

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

### <span data-ttu-id="e56c9-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e56c9-129">-InformationVariable</span></span>
<span data-ttu-id="e56c9-130">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="e56c9-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e56c9-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="e56c9-131">-Profile</span></span>
<span data-ttu-id="e56c9-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e56c9-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e56c9-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e56c9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e56c9-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e56c9-134">-ServiceName</span></span>
<span data-ttu-id="e56c9-135">Указывает имя службы, для которой этот командлет удаляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="e56c9-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="e56c9-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="e56c9-136">-Slot</span></span>
<span data-ttu-id="e56c9-137">Указывает среду развертывания, из которой этот командлет удаляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="e56c9-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="e56c9-138">Допустимые значения: промежуточные и производственные.</span><span class="sxs-lookup"><span data-stu-id="e56c9-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="e56c9-139">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="e56c9-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e56c9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e56c9-140">CommonParameters</span></span>
<span data-ttu-id="e56c9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e56c9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e56c9-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e56c9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e56c9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e56c9-143">INPUTS</span></span>

## <span data-ttu-id="e56c9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e56c9-144">OUTPUTS</span></span>

### <span data-ttu-id="e56c9-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e56c9-145">ManagementOperationContext</span></span>

## <span data-ttu-id="e56c9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="e56c9-146">NOTES</span></span>

## <span data-ttu-id="e56c9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e56c9-147">RELATED LINKS</span></span>

[<span data-ttu-id="e56c9-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e56c9-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="e56c9-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="e56c9-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="e56c9-150">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e56c9-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="e56c9-151">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e56c9-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="e56c9-152">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e56c9-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


