---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 81acbdd914d4a3cdb69da9ac0d2093f4e1dd4cdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721754"
---
# <span data-ttu-id="bd13b-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bd13b-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="bd13b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd13b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd13b-103">Удаляет расширение SQL Server из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bd13b-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="bd13b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd13b-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd13b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd13b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd13b-106">Командлет **Remove-AzVMSqlServerExtension** удаляет расширение сервера AzureSQL из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bd13b-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="bd13b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd13b-107">EXAMPLES</span></span>

### <span data-ttu-id="bd13b-108">Пример 1: удаление расширения SQL Server</span><span class="sxs-lookup"><span data-stu-id="bd13b-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="bd13b-109">Эта команда удаляет расширение SQL Server из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="bd13b-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="bd13b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd13b-110">PARAMETERS</span></span>

### <span data-ttu-id="bd13b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd13b-111">-DefaultProfile</span></span>
<span data-ttu-id="bd13b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd13b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd13b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd13b-113">-Name</span></span>
<span data-ttu-id="bd13b-114">Указывает имя сервера SQL Server, расширение которого удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bd13b-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd13b-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="bd13b-115">-NoWait</span></span>
<span data-ttu-id="bd13b-116">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="bd13b-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bd13b-117">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="bd13b-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bd13b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd13b-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd13b-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bd13b-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bd13b-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="bd13b-120">-VMName</span></span>
<span data-ttu-id="bd13b-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bd13b-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd13b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd13b-122">CommonParameters</span></span>
<span data-ttu-id="bd13b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd13b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd13b-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd13b-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd13b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd13b-125">INPUTS</span></span>

### <span data-ttu-id="bd13b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bd13b-126">System.String</span></span>

## <span data-ttu-id="bd13b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd13b-127">OUTPUTS</span></span>

### <span data-ttu-id="bd13b-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bd13b-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bd13b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd13b-129">NOTES</span></span>

## <span data-ttu-id="bd13b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd13b-130">RELATED LINKS</span></span>

[<span data-ttu-id="bd13b-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bd13b-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="bd13b-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="bd13b-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


