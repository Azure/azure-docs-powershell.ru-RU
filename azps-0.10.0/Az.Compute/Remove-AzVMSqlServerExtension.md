---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 6e3803b7627e16a96c8101f3a6dd1eee5a1b2689
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911406"
---
# <span data-ttu-id="f5f9d-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f5f9d-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="f5f9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f9d-103">Удаляет расширение SQL Server из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="f5f9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5f9d-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f9d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f9d-106">Командлет **Remove-AzVMSqlServerExtension** удаляет расширение сервера AzureSQL из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="f5f9d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f9d-108">Пример 1: удаление расширения SQL Server</span><span class="sxs-lookup"><span data-stu-id="f5f9d-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="f5f9d-109">Эта команда удаляет расширение SQL Server из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="f5f9d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="f5f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="f5f9d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f9d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5f9d-113">-Name</span></span>
<span data-ttu-id="f5f9d-114">Указывает имя сервера SQL Server, расширение которого удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5f9d-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f5f9d-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="f5f9d-117">-VMName</span></span>
<span data-ttu-id="f5f9d-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f9d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f9d-119">CommonParameters</span></span>
<span data-ttu-id="f5f9d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f9d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f9d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f9d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5f9d-122">INPUTS</span></span>

### <span data-ttu-id="f5f9d-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5f9d-123">None</span></span>
<span data-ttu-id="f5f9d-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f5f9d-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5f9d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5f9d-125">OUTPUTS</span></span>

### <span data-ttu-id="f5f9d-126">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f5f9d-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f5f9d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5f9d-127">NOTES</span></span>

## <span data-ttu-id="f5f9d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5f9d-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5f9d-129">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f5f9d-129">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="f5f9d-130">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f5f9d-130">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


