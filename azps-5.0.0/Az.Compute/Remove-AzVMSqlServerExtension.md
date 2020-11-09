---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318656"
---
# <span data-ttu-id="5bf3c-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5bf3c-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="5bf3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf3c-103">Удаляет расширение SQL Server из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="5bf3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bf3c-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bf3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf3c-106">Командлет **Remove-AzVMSqlServerExtension** удаляет расширение сервера AzureSQL из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="5bf3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf3c-108">Пример 1: удаление расширения SQL Server</span><span class="sxs-lookup"><span data-stu-id="5bf3c-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="5bf3c-109">Эта команда удаляет расширение SQL Server из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="5bf3c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-110">PARAMETERS</span></span>

### <span data-ttu-id="5bf3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf3c-111">-DefaultProfile</span></span>
<span data-ttu-id="5bf3c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bf3c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5bf3c-113">-Name</span></span>
<span data-ttu-id="5bf3c-114">Указывает имя сервера SQL Server, расширение которого удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5bf3c-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="5bf3c-115">-NoWait</span></span>
<span data-ttu-id="5bf3c-116">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5bf3c-117">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5bf3c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf3c-118">-ResourceGroupName</span></span>
<span data-ttu-id="5bf3c-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5bf3c-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="5bf3c-120">-VMName</span></span>
<span data-ttu-id="5bf3c-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="5bf3c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf3c-122">CommonParameters</span></span>
<span data-ttu-id="5bf3c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bf3c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf3c-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bf3c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf3c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bf3c-125">INPUTS</span></span>

### <span data-ttu-id="5bf3c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf3c-126">System.String</span></span>

## <span data-ttu-id="5bf3c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-127">OUTPUTS</span></span>

### <span data-ttu-id="5bf3c-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5bf3c-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5bf3c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bf3c-129">NOTES</span></span>

## <span data-ttu-id="5bf3c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bf3c-130">RELATED LINKS</span></span>

[<span data-ttu-id="5bf3c-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5bf3c-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="5bf3c-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5bf3c-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


