---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245615"
---
# <span data-ttu-id="7d311-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7d311-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="7d311-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d311-102">SYNOPSIS</span></span>
<span data-ttu-id="7d311-103">Получает параметры для расширения SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7d311-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="7d311-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d311-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d311-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d311-105">DESCRIPTION</span></span>
<span data-ttu-id="7d311-106">Командлет **Get-AzVMSqlServerExtension** получает параметры инфраструктуры SQL Server как агента службы (IaaS) на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7d311-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="7d311-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d311-107">EXAMPLES</span></span>

### <span data-ttu-id="7d311-108">Пример 1: получение параметров расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="7d311-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="7d311-109">Эта команда получает параметры расширения SQL Server на виртуальной машине с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="7d311-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="7d311-110">Пример 2: получение параметров с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="7d311-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="7d311-111">Эта команда получает виртуальную машину с именем ContosoVM22 в службе Service08 с помощью командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7d311-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="7d311-112">Команда передает результаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="7d311-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d311-113">Текущая команда получает параметры агента SQL Server IaaS на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="7d311-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="7d311-114">Пример 3: получение параметров для конкретной версии SQL Server</span><span class="sxs-lookup"><span data-stu-id="7d311-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="7d311-115">Эта команда получает параметры версии 1,0 расширения SQL Server на виртуальной машине с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="7d311-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="7d311-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d311-116">PARAMETERS</span></span>

### <span data-ttu-id="7d311-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d311-117">-DefaultProfile</span></span>
<span data-ttu-id="7d311-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d311-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d311-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d311-119">-Name</span></span>
<span data-ttu-id="7d311-120">Указывает имя сервера SQL Server, на котором находится расширение.</span><span class="sxs-lookup"><span data-stu-id="7d311-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d311-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d311-121">-ResourceGroupName</span></span>
<span data-ttu-id="7d311-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7d311-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7d311-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="7d311-123">-VMName</span></span>
<span data-ttu-id="7d311-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7d311-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7d311-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d311-125">CommonParameters</span></span>
<span data-ttu-id="7d311-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d311-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d311-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d311-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d311-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d311-128">INPUTS</span></span>

### <span data-ttu-id="7d311-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7d311-129">System.String</span></span>

## <span data-ttu-id="7d311-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d311-130">OUTPUTS</span></span>

### <span data-ttu-id="7d311-131">Microsoft. Azure. Commands. COMPUTE. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="7d311-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="7d311-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d311-132">NOTES</span></span>

## <span data-ttu-id="7d311-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d311-133">RELATED LINKS</span></span>

[<span data-ttu-id="7d311-134">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7d311-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7d311-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7d311-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="7d311-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7d311-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

