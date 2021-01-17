---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 7d3cd39a18f7cbbd9663d656921375daa490b32e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395799"
---
# <span data-ttu-id="f4b2b-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f4b2b-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="f4b2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b2b-103">Создает управляемое HSM.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="f4b2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4b2b-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4b2b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b2b-106">**Новый-AzKeyVaultManagedHsm** создает управляемый HSM в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="f4b2b-107">Чтобы добавить, удалить или удалить ключи списков в управляемой HSM, пользователю следует предоставить разрешения, добавив ИД пользователя к администратору.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="f4b2b-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4b2b-108">EXAMPLES</span></span>

### <span data-ttu-id="f4b2b-109">Пример 1. Создание управляемой HSM standardB1</span><span class="sxs-lookup"><span data-stu-id="f4b2b-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="f4b2b-110">Эта команда создает управляемую HSM с именем myhsm в расположении eastus2euap.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="f4b2b-111">Команда добавляет управляемый HSM в группу ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="f4b2b-112">Так как команда не указывает значение параметра *SKU,* она создает Standard_B1 управляемой HSM.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="f4b2b-113">Пример 2. Создание управляемой HSM-возможности CustomB32</span><span class="sxs-lookup"><span data-stu-id="f4b2b-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="f4b2b-114">Эта команда создает управляемый HSM, как в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="f4b2b-115">Однако она указывает значение CustomB32 для параметра *SKU,* чтобы создать настраиваемый HSM, управляемый CustomB32.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="f4b2b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4b2b-116">PARAMETERS</span></span>

### <span data-ttu-id="f4b2b-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="f4b2b-117">-Administrator</span></span>
<span data-ttu-id="f4b2b-118">ИД объекта начального администратора для этого управляемого пула HSM.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="f4b2b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4b2b-119">-AsJob</span></span>
<span data-ttu-id="f4b2b-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4b2b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4b2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b2b-121">-DefaultProfile</span></span>
<span data-ttu-id="f4b2b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b2b-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f4b2b-123">-Location</span></span>
<span data-ttu-id="f4b2b-124">Определяет регион Azure, в котором нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="f4b2b-125">Используйте команду Get-AzResourceProvider с параметром ProviderNamespace, чтобы увидеть ваши варианты.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="f4b2b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f4b2b-126">-Name</span></span>
<span data-ttu-id="f4b2b-127">Имя управляемой службы HSM, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="f4b2b-128">Имя может быть любым сочетанием букв, цифр или дефисов.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="f4b2b-129">Имя должно начинаться с буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="f4b2b-130">Имя должно быть универсальным.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="f4b2b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b2b-131">-ResourceGroupName</span></span>
<span data-ttu-id="f4b2b-132">Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="f4b2b-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="f4b2b-133">-Sku</span></span>
<span data-ttu-id="f4b2b-134">Указывает SKU управляемого экземпляра HSM.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="f4b2b-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4b2b-135">-Tag</span></span>
<span data-ttu-id="f4b2b-136">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f4b2b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4b2b-137">-Confirm</span></span>
<span data-ttu-id="f4b2b-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b2b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b2b-139">-WhatIf</span></span>
<span data-ttu-id="f4b2b-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4b2b-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b2b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b2b-142">CommonParameters</span></span>
<span data-ttu-id="f4b2b-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b2b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b2b-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4b2b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b2b-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4b2b-145">INPUTS</span></span>

### <span data-ttu-id="f4b2b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="f4b2b-146">System.String</span></span>

### <span data-ttu-id="f4b2b-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f4b2b-147">System.String[]</span></span>

### <span data-ttu-id="f4b2b-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4b2b-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4b2b-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4b2b-149">OUTPUTS</span></span>

### <span data-ttu-id="f4b2b-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f4b2b-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="f4b2b-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4b2b-151">NOTES</span></span>

## <span data-ttu-id="f4b2b-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4b2b-152">RELATED LINKS</span></span>

[<span data-ttu-id="f4b2b-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f4b2b-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="f4b2b-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f4b2b-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="f4b2b-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="f4b2b-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)