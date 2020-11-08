---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076126"
---
# <span data-ttu-id="76df6-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="76df6-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="76df6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76df6-102">SYNOPSIS</span></span>
<span data-ttu-id="76df6-103">Удаляет расширение доменных имен AD облачных служб, примененное ко всем ролям или именованным ролям, в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="76df6-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="76df6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76df6-104">SYNTAX</span></span>

### <span data-ttu-id="76df6-105">RemoveByRoles (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76df6-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="76df6-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="76df6-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="76df6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76df6-107">DESCRIPTION</span></span>
<span data-ttu-id="76df6-108">Командлет **Remove-AzureServiceADDomainExtension** удаляет расширение доменной службы Active Directory (AD), примененное на всех ролях или именованных ролях, в определенном слоте развертывания.</span><span class="sxs-lookup"><span data-stu-id="76df6-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="76df6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76df6-109">EXAMPLES</span></span>

### <span data-ttu-id="76df6-110">Пример 1: удаление расширения доменной рекламы</span><span class="sxs-lookup"><span data-stu-id="76df6-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="76df6-111">Эта команда удаляет расширение, указанное переменной $Svc.</span><span class="sxs-lookup"><span data-stu-id="76df6-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="76df6-112">Пример 2: удаление расширения доменной службы для указанной роли</span><span class="sxs-lookup"><span data-stu-id="76df6-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="76df6-113">Эта команда удаляет расширение службы для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="76df6-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="76df6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76df6-114">PARAMETERS</span></span>

### <span data-ttu-id="76df6-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="76df6-115">-InformationAction</span></span>
<span data-ttu-id="76df6-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="76df6-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="76df6-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="76df6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="76df6-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="76df6-118">Continue</span></span>
- <span data-ttu-id="76df6-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="76df6-119">Ignore</span></span>
- <span data-ttu-id="76df6-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="76df6-120">Inquire</span></span>
- <span data-ttu-id="76df6-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="76df6-121">SilentlyContinue</span></span>
- <span data-ttu-id="76df6-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="76df6-122">Stop</span></span>
- <span data-ttu-id="76df6-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="76df6-123">Suspend</span></span>

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

### <span data-ttu-id="76df6-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="76df6-124">-InformationVariable</span></span>
<span data-ttu-id="76df6-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="76df6-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="76df6-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="76df6-126">-Profile</span></span>
<span data-ttu-id="76df6-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="76df6-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="76df6-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76df6-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="76df6-129">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="76df6-129">-Role</span></span>
<span data-ttu-id="76df6-130">Задает необязательный массив ролей, для которого нужно задать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="76df6-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="76df6-131">Если не указано, Конфигурация домена AD применяется в качестве конфигурации по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="76df6-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76df6-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="76df6-132">-ServiceName</span></span>
<span data-ttu-id="76df6-133">Указывает имя службы Azure.</span><span class="sxs-lookup"><span data-stu-id="76df6-133">Specifies the name of an Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76df6-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="76df6-134">-Slot</span></span>
<span data-ttu-id="76df6-135">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="76df6-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="76df6-136">Допустимые значения: Production или промежуточный.</span><span class="sxs-lookup"><span data-stu-id="76df6-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="76df6-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="76df6-137">-UninstallConfiguration</span></span>
<span data-ttu-id="76df6-138">Указывает, что этот командлет удаляет все конфигурации доменных служб Active Directory из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="76df6-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76df6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76df6-139">CommonParameters</span></span>
<span data-ttu-id="76df6-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76df6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76df6-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76df6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76df6-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76df6-142">INPUTS</span></span>

## <span data-ttu-id="76df6-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76df6-143">OUTPUTS</span></span>

## <span data-ttu-id="76df6-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="76df6-144">NOTES</span></span>

## <span data-ttu-id="76df6-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76df6-145">RELATED LINKS</span></span>

[<span data-ttu-id="76df6-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="76df6-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="76df6-147">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="76df6-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


