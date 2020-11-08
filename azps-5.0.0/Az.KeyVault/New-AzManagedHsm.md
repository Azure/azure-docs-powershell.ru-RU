---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250210"
---
# <span data-ttu-id="73fdc-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="73fdc-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="73fdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="73fdc-103">Создает управляемый HSM-аппарат.</span><span class="sxs-lookup"><span data-stu-id="73fdc-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="73fdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73fdc-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73fdc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="73fdc-106">Командлет **New-AzManagedHsm** создает управляемый HSM в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73fdc-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="73fdc-107">Чтобы добавить, удалить или перечислить ключи в управляемом HSM, пользователю необходимо предоставить разрешения, добавив идентификатор пользователя для администратора.</span><span class="sxs-lookup"><span data-stu-id="73fdc-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="73fdc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73fdc-108">EXAMPLES</span></span>

### <span data-ttu-id="73fdc-109">Пример 1: создание управляемого HSM StandardB1</span><span class="sxs-lookup"><span data-stu-id="73fdc-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="73fdc-110">Эта команда создает управляемый HSM-интерфейс с именем myhsm в eastus2euap расположении.</span><span class="sxs-lookup"><span data-stu-id="73fdc-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="73fdc-111">Команда добавляет управляемый HSM – in в группу ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="73fdc-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="73fdc-112">Поскольку в команде не указано значение параметра *SKU* , создается Standard_B1 управляемый HSM-файл.</span><span class="sxs-lookup"><span data-stu-id="73fdc-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="73fdc-113">Пример 2: создание управляемого HSM CustomB32</span><span class="sxs-lookup"><span data-stu-id="73fdc-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="73fdc-114">Эта команда создает управляемый HSM-код, как и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="73fdc-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="73fdc-115">Однако он задает значение CustomB32 для параметра *SKU* для создания CustomB32 управляемого HSM-файла.</span><span class="sxs-lookup"><span data-stu-id="73fdc-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="73fdc-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73fdc-116">PARAMETERS</span></span>

### <span data-ttu-id="73fdc-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="73fdc-117">-Administrator</span></span>
<span data-ttu-id="73fdc-118">Идентификатор начального объекта администратора для этого управляемого пула HSM.</span><span class="sxs-lookup"><span data-stu-id="73fdc-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73fdc-119">-AsJob</span></span>
<span data-ttu-id="73fdc-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="73fdc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73fdc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fdc-121">-DefaultProfile</span></span>
<span data-ttu-id="73fdc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73fdc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73fdc-123">-Location</span><span class="sxs-lookup"><span data-stu-id="73fdc-123">-Location</span></span>
<span data-ttu-id="73fdc-124">Указывает область Azure, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="73fdc-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="73fdc-125">Используйте командную Get-AzResourceProvider с параметром ProviderNamespace, чтобы просмотреть варианты выбора.</span><span class="sxs-lookup"><span data-stu-id="73fdc-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73fdc-126">-Name</span></span>
<span data-ttu-id="73fdc-127">Задает имя создаваемого управляемого HSM-файла.</span><span class="sxs-lookup"><span data-stu-id="73fdc-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="73fdc-128">Имя может представлять собой любую комбинацию букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="73fdc-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="73fdc-129">Имя должно начинаться и заканчиваться на букву или цифру.</span><span class="sxs-lookup"><span data-stu-id="73fdc-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="73fdc-130">Имя должно быть универсальным уникальным.</span><span class="sxs-lookup"><span data-stu-id="73fdc-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73fdc-131">-ResourceGroupName</span></span>
<span data-ttu-id="73fdc-132">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="73fdc-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="73fdc-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="73fdc-133">-Sku</span></span>
<span data-ttu-id="73fdc-134">Указывает SKU управляемого экземпляра HSM.</span><span class="sxs-lookup"><span data-stu-id="73fdc-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="73fdc-135">-Tag</span></span>
<span data-ttu-id="73fdc-136">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73fdc-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73fdc-137">-Confirm</span></span>
<span data-ttu-id="73fdc-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73fdc-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73fdc-139">-WhatIf</span></span>
<span data-ttu-id="73fdc-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73fdc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73fdc-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73fdc-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73fdc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fdc-142">CommonParameters</span></span>
<span data-ttu-id="73fdc-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73fdc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fdc-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73fdc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fdc-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73fdc-145">INPUTS</span></span>

### <span data-ttu-id="73fdc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="73fdc-146">System.String</span></span>

### <span data-ttu-id="73fdc-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="73fdc-147">System.String[]</span></span>

### <span data-ttu-id="73fdc-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="73fdc-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="73fdc-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73fdc-149">OUTPUTS</span></span>

### <span data-ttu-id="73fdc-150">Microsoft. Azure. Commands. KeyVault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="73fdc-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="73fdc-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="73fdc-151">NOTES</span></span>

## <span data-ttu-id="73fdc-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73fdc-152">RELATED LINKS</span></span>

[<span data-ttu-id="73fdc-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="73fdc-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="73fdc-154">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="73fdc-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="73fdc-155">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="73fdc-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)