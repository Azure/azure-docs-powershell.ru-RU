---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075530"
---
# <span data-ttu-id="25e0f-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="25e0f-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="25e0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="25e0f-103">Получает параметры агента IaaS SQL Server на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="25e0f-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="25e0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25e0f-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="25e0f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25e0f-105">DESCRIPTION</span></span>
<span data-ttu-id="25e0f-106">Командлет **Get-AzureVMSqlServerExtension** получает параметры инфраструктуры SQL Server как агента службы (IaaS) на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="25e0f-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="25e0f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25e0f-107">EXAMPLES</span></span>

### <span data-ttu-id="25e0f-108">Пример 1: получение параметров расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="25e0f-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="25e0f-109">Получает параметры расширения SQL Server для определенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="25e0f-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="25e0f-110">Пример 2: получение параметров агента IaaS SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="25e0f-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="25e0f-111">Получает параметры агента IaaS SQL Server на определенной виртуальной машине с помощью передающего входных данных.</span><span class="sxs-lookup"><span data-stu-id="25e0f-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="25e0f-112">Пример 3: получение параметров конкретного агента IaaS SQL Server версии на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="25e0f-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="25e0f-113">Эта команда получает параметры конкретной версии агента SQL Server IaaS на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="25e0f-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="25e0f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25e0f-114">PARAMETERS</span></span>

### <span data-ttu-id="25e0f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="25e0f-115">-InformationAction</span></span>
<span data-ttu-id="25e0f-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="25e0f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="25e0f-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="25e0f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25e0f-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="25e0f-118">Continue</span></span>
- <span data-ttu-id="25e0f-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="25e0f-119">Ignore</span></span>
- <span data-ttu-id="25e0f-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="25e0f-120">Inquire</span></span>
- <span data-ttu-id="25e0f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="25e0f-121">SilentlyContinue</span></span>
- <span data-ttu-id="25e0f-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="25e0f-122">Stop</span></span>
- <span data-ttu-id="25e0f-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="25e0f-123">Suspend</span></span>

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

### <span data-ttu-id="25e0f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="25e0f-124">-InformationVariable</span></span>
<span data-ttu-id="25e0f-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="25e0f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="25e0f-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="25e0f-126">-Profile</span></span>
<span data-ttu-id="25e0f-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25e0f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25e0f-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25e0f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25e0f-129">-VM</span><span class="sxs-lookup"><span data-stu-id="25e0f-129">-VM</span></span>
<span data-ttu-id="25e0f-130">Указывает Сохраняемый объект виртуальной машины, из которого этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="25e0f-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e0f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e0f-131">CommonParameters</span></span>
<span data-ttu-id="25e0f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25e0f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e0f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e0f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e0f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25e0f-134">INPUTS</span></span>

## <span data-ttu-id="25e0f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25e0f-135">OUTPUTS</span></span>

## <span data-ttu-id="25e0f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="25e0f-136">NOTES</span></span>

## <span data-ttu-id="25e0f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25e0f-137">RELATED LINKS</span></span>

[<span data-ttu-id="25e0f-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="25e0f-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="25e0f-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="25e0f-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


