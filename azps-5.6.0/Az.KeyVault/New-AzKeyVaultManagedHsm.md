---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 72804d546869f2d003813c8e69c067ad23966fa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001304"
---
# <span data-ttu-id="ed063-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ed063-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="ed063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed063-102">SYNOPSIS</span></span>
<span data-ttu-id="ed063-103">Создает управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="ed063-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="ed063-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed063-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed063-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed063-105">DESCRIPTION</span></span>
<span data-ttu-id="ed063-106">Для **создания управляемой** HSM в указанной группе ресурсов будет создаваться управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="ed063-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="ed063-107">Чтобы добавить, удалить или удалить ключи списков в управляемой HSM, пользователю следует предоставить разрешения, добавив ИД пользователя к администратору.</span><span class="sxs-lookup"><span data-stu-id="ed063-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="ed063-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed063-108">EXAMPLES</span></span>

### <span data-ttu-id="ed063-109">Пример 1. Создание управляемой HSM standardB1</span><span class="sxs-lookup"><span data-stu-id="ed063-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="ed063-110">Эта команда создает управляемый HSM с именем myhsm в расположении eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="ed063-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="ed063-111">Команда добавляет управляемый HSM в группу ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="ed063-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="ed063-112">Так как команда не указывает значение параметра *SKU,* она создает Standard_B1 HSM.</span><span class="sxs-lookup"><span data-stu-id="ed063-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="ed063-113">Пример 2. Создание управляемой HSM-возможности CustomB32</span><span class="sxs-lookup"><span data-stu-id="ed063-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="ed063-114">Эта команда создает управляемый HSM, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="ed063-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="ed063-115">Однако она указывает значение CustomB32 для параметра *SKU,* чтобы создать настраиваемый HSM, управляемый CustomB32.</span><span class="sxs-lookup"><span data-stu-id="ed063-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="ed063-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed063-116">PARAMETERS</span></span>

### <span data-ttu-id="ed063-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="ed063-117">-Administrator</span></span>
<span data-ttu-id="ed063-118">ИД объекта начального администратора для этого управляемого пула HSM.</span><span class="sxs-lookup"><span data-stu-id="ed063-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="ed063-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed063-119">-AsJob</span></span>
<span data-ttu-id="ed063-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ed063-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed063-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed063-121">-DefaultProfile</span></span>
<span data-ttu-id="ed063-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed063-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed063-123">-Location</span><span class="sxs-lookup"><span data-stu-id="ed063-123">-Location</span></span>
<span data-ttu-id="ed063-124">Определяет регион Azure, в котором нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ed063-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="ed063-125">Используйте команду Get-AzResourceProvider с параметром ProviderNamespace, чтобы увидеть ваши варианты.</span><span class="sxs-lookup"><span data-stu-id="ed063-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="ed063-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ed063-126">-Name</span></span>
<span data-ttu-id="ed063-127">Имя управляемой службы HSM, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="ed063-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="ed063-128">Имя может быть любым сочетанием букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="ed063-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="ed063-129">Имя должно начинаться с буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="ed063-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="ed063-130">Имя должно быть универсальным.</span><span class="sxs-lookup"><span data-stu-id="ed063-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="ed063-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed063-131">-ResourceGroupName</span></span>
<span data-ttu-id="ed063-132">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ed063-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="ed063-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="ed063-133">-Sku</span></span>
<span data-ttu-id="ed063-134">Указывает SKU управляемого экземпляра HSM.</span><span class="sxs-lookup"><span data-stu-id="ed063-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="ed063-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed063-135">-Tag</span></span>
<span data-ttu-id="ed063-136">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="ed063-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ed063-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed063-137">-Confirm</span></span>
<span data-ttu-id="ed063-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ed063-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed063-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed063-139">-WhatIf</span></span>
<span data-ttu-id="ed063-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed063-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed063-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ed063-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed063-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed063-142">CommonParameters</span></span>
<span data-ttu-id="ed063-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed063-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed063-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed063-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed063-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed063-145">INPUTS</span></span>

### <span data-ttu-id="ed063-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ed063-146">System.String</span></span>

### <span data-ttu-id="ed063-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ed063-147">System.String[]</span></span>

### <span data-ttu-id="ed063-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ed063-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ed063-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed063-149">OUTPUTS</span></span>

### <span data-ttu-id="ed063-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ed063-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="ed063-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed063-151">NOTES</span></span>

## <span data-ttu-id="ed063-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed063-152">RELATED LINKS</span></span>

[<span data-ttu-id="ed063-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ed063-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="ed063-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ed063-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="ed063-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="ed063-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)