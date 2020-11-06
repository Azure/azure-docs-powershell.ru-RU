---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 94c93410692c71b16150b2078f764f5b96c71e6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568819"
---
# <span data-ttu-id="0349c-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0349c-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="0349c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0349c-102">SYNOPSIS</span></span>
<span data-ttu-id="0349c-103">Получает параметры для расширения SQL Server на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0349c-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0349c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0349c-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0349c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0349c-105">DESCRIPTION</span></span>
<span data-ttu-id="0349c-106">Командлет **Get-AzureRmVMSqlServerExtension** получает параметры инфраструктуры SQL Server как агента службы (IaaS) на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0349c-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="0349c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0349c-107">EXAMPLES</span></span>

### <span data-ttu-id="0349c-108">Пример 1: получение параметров расширения SQL Server на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="0349c-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="0349c-109">Эта команда получает параметры расширения SQL Server на виртуальной машине с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="0349c-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="0349c-110">Пример 2: получение параметров с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="0349c-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="0349c-111">Эта команда получает виртуальную машину с именем ContosoVM22 в службе Service08 с помощью командлета Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="0349c-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="0349c-112">Команда передает результаты в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="0349c-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="0349c-113">Текущая команда получает параметры агента SQL Server IaaS на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0349c-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="0349c-114">Пример 3: получение параметров для конкретной версии SQL Server</span><span class="sxs-lookup"><span data-stu-id="0349c-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="0349c-115">Эта команда получает параметры версии 1,0 расширения SQL Server на виртуальной машине с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="0349c-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="0349c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0349c-116">PARAMETERS</span></span>

### <span data-ttu-id="0349c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0349c-117">-DefaultProfile</span></span>
<span data-ttu-id="0349c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0349c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0349c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0349c-119">-Name</span></span>
<span data-ttu-id="0349c-120">Указывает имя сервера SQL Server, на котором находится расширение.</span><span class="sxs-lookup"><span data-stu-id="0349c-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="0349c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0349c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0349c-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0349c-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0349c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0349c-123">-VMName</span></span>
<span data-ttu-id="0349c-124">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0349c-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0349c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0349c-125">CommonParameters</span></span>
<span data-ttu-id="0349c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0349c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0349c-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0349c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0349c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0349c-128">INPUTS</span></span>

## <span data-ttu-id="0349c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0349c-129">OUTPUTS</span></span>

## <span data-ttu-id="0349c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="0349c-130">NOTES</span></span>

## <span data-ttu-id="0349c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0349c-131">RELATED LINKS</span></span>

[<span data-ttu-id="0349c-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0349c-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0349c-133">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0349c-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="0349c-134">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0349c-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


