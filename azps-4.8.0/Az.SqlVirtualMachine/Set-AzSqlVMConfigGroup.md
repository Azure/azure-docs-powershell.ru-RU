---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: b83dc58161791009a3adfd7cbf9b0b07b3f0b5b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236562"
---
# <span data-ttu-id="b4cbb-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="b4cbb-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="b4cbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cbb-103">Укажите сведения, относящиеся к группе виртуальных машин SQL, в конфигурации виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="b4cbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4cbb-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4cbb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4cbb-105">DESCRIPTION</span></span>
<span data-ttu-id="b4cbb-106">Командлет Set-AzSqlVMConfigGroup задает сведения, необходимые для присоединения к группе виртуальных машин SQL для конфигурации виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="b4cbb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4cbb-107">EXAMPLES</span></span>

### <span data-ttu-id="b4cbb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b4cbb-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="b4cbb-109">Обновите сведения о группе для конфигурации виртуальной машины SQL.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="b4cbb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4cbb-110">PARAMETERS</span></span>

### <span data-ttu-id="b4cbb-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="b4cbb-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="b4cbb-112">Пароль для учетной записи начальной загрузки кластера</span><span class="sxs-lookup"><span data-stu-id="b4cbb-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cbb-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="b4cbb-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="b4cbb-114">Пароль для учетной записи оператора кластера</span><span class="sxs-lookup"><span data-stu-id="b4cbb-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cbb-115">-DefaultProfile</span></span>
<span data-ttu-id="b4cbb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4cbb-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="b4cbb-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="b4cbb-118">Пароль для учетной записи службы SQL</span><span class="sxs-lookup"><span data-stu-id="b4cbb-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cbb-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="b4cbb-119">-SqlVM</span></span>
<span data-ttu-id="b4cbb-120">Конфигурация виртуальной машины SQL, в которую будут добавлены сведения о членстве в группах</span><span class="sxs-lookup"><span data-stu-id="b4cbb-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4cbb-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="b4cbb-121">-SqlVMGroup</span></span>
<span data-ttu-id="b4cbb-122">Группа, в которую будет входить виртуальная машина SQL</span><span class="sxs-lookup"><span data-stu-id="b4cbb-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4cbb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cbb-123">CommonParameters</span></span>
<span data-ttu-id="b4cbb-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4cbb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cbb-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4cbb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cbb-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4cbb-126">INPUTS</span></span>

### <span data-ttu-id="b4cbb-127">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b4cbb-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b4cbb-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4cbb-128">OUTPUTS</span></span>

### <span data-ttu-id="b4cbb-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="b4cbb-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="b4cbb-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4cbb-130">NOTES</span></span>

## <span data-ttu-id="b4cbb-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4cbb-131">RELATED LINKS</span></span>
